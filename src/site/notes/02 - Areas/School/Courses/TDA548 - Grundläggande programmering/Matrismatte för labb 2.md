---
{"dg-publish":true,"dg-path":"TDA548 - Grundläggande programmering/Matrismatte för labb 2.md","permalink":"/TDA548 - Grundläggande programmering/Matrismatte för labb 2/"}
---

Först och främst, det här är min egen förklaring med direkt anknytning till programmeringen där jag skummar över detaljer som inte är nödvändiga för vår implementation. Om du vill läsa mer om matrismatte är det sidor 322–337 i [diskret-matteboken](https://www.chalmersstore.se/svensk-litteratur/algebra-och-diskret-matematik.html).

## Vad är en matris?

En *matris* är en tabell av *element* som har ett antal *rader* och *kolumner*.

En matris $A=\left[\begin{array}{cc} 1 &2 &3 \\ 4 &5 &6 \end{array}\right]$ har 2 rader och 3 kolumner. Man kan även säga att $A$ är av typen $2\times3$ eller att $A$ har *dimensionen* $(2,3)$.

Ett elementet på rad $i$ och kolumn $j$ i matrisen $A$ betecknas $A_{ij}$
I matrisen ovan är t.ex. $A_{21}=4$

## Matriser inom programmering

I Python representerar vi en matris som en lista av rader, vilket i sin tur är en lista av element.

```python
matris = [[3, 2],
          [1, 4]]
```

Här är en rad ett element i listan `matris` (`[3, 2]` eller `[1, 4]`), **antalet rader** i matrisen är därför längden av listan `len(matris)`.

> [!Warning] OBS: Element kan ha flera betydelser
> 
> Lägg märke till ordet *element* kan ha flera betydelser i det här sammanhanget:
> 
> - Ett värde i en Python-lista på ett **index**.
> - Ett värde i en matris på en **rad och kolumn**.

Att få ut en kolumn (`[3, 1]` eller `[2, 4]`) är inte lika enkelt som en rad eftersom en kolumn sträcker sig över flera listor. Som tur är kommer vi inte behöva det här eftersom vi endast kommer räkna på ett element i taget.

**Antalet kolumner** i matrisen är längden av våra rader. Vi tar värdet från den första raden för enkelhetens skull och får därför antalet kolumner med uttrycket: `len(matris[0])`.

För att få värdet av ett element i matrisen på rad `i` och kolumn `j` används den här koden:

```python
matris  = [[3, 2],
           [1, 4]]

i = 0
j = 1

element = matris[i][j]
print(element) # Ger oss värdet 2
```

> [!note] Förklaring
> Uttrycket `matris[i]` ger oss rad `i` i matrisen. Här är `i = 0` vilket innebär att `matris[i] == [3, 2]`. Efter detta tar vi elementet på indexet `j` i raden: `matris[i][j] == matris[0][1] == [3, 2][1] == 2`.
> 
> Lägg även märke till att matriser i Python börjar med rad och kolumn 0.

## Transponat

Ett *transponat* av en matris $A$ noteras som $A^T$ och innebär att raderna och kolumnerna byts.

T.ex:

$A=\left[\begin{array}{cc}1 &2 &3\\ 4 &5 &6\end{array}\right]$

$A^T=\left[\begin{array}{cc}1 &4\\ 2 &5\\ 3 &6\end{array}\right]$

Ett element i den transponerade matrisen definieras som $A^T_{ij}=A_{ji}$

### Algoritmen för matrisoperationer

Detta här är algoritmen vi kommer använda för våra matrisoperationer:

1. Definiera dimensionerna av våra inmatade matriser.
2. Kontrollera att de inmatade matriserna är av godtycklig typ om applicerbart.
3. Skapa en tom matris med rätt dimensioner.
4. Iterera genom varje rad i matrisen:
	1. Iterera genom varje element på raden och beräkna det nya värdet.

#### Skapa en tom matris

För att skapa en ny matris *C* av typen $m\times n$ använder följande uttryck:

```python
C = [[0]*n for _ in range(m)]
```

För att första detta uttryck behöver vi lära oss *listmultiplikation* och *listkonkatenering*:

##### Listmultiplikation

**Listmultiplikation** låter oss upprepa en lista ett visst antal gånger och används som följer:

```python
[1, 2, 3] * 2 # = [1, 2, 3, 1, 2, 3]
['a', 'b'] * 4 # = ['a', 'b', 'a', 'b', 'a', 'b', 'a', 'b']
```

##### Listkonkatenering

**Listkonkatenering** tar alla värden i en lista och skapar en ny lista. Det kan dels användas för att skapa en kopia av en lista, men är verkligen användbart tillsammans med ett *uttryck* som ger varje element ett nytt värde utifrån värdet i den ursprungliga listan. Listkonkatenering skrivs som `[uttryck for x in a]` där *a* är den urprungliga listan och *x* är en variabel som antar värdet av varje element i listan *a*. `uttryck` ersätts med ett utryck som modifierar *x* på något sätt, t.ex. `x*2` eller `ord(x)`.

Här är ett exempel på listkonkatenering och dess resultat:

```python
a = [1, 2, 3]
[x*2 for x in a] # = [2, 4, 6]
```

##### Vårt slutliga uttryck

```python
C = [[0]*n for _ in range(m)]
```

Uttrycket `[0]*n` skapar en *rad* i vår matris där *n* är antalet kolumner. Om t.ex. *n* är **3** så blir en rad `[0, 0, 0]`.

För att skapa fler rader använder vi [[02 - Areas/School/Courses/TDA548 - Grundläggande programmering/Matrismatte för labb 2#listkonkatenering\|#listkonkatenering]]. Eftersom listkonkatenering skapar en lista av samma längd som den som matas in och vi vill att vår "matrislista" ska ha *m* element (rader) måste även den inmatade listan vara av längd *m*. Det görs enklast med den inbyggda `range(m)` funktionen i Python som skapar en lista `[0, 1,..., m-1]` vilket alltid har längden *m* om vi endast anger en parameter. Eftersom vi inte bryr oss om **elementen** i den ursprungliga listan (`range(m)`) utan endast **längden** av listan använder vi `_` som vår variabel vilket säger till Python att ignorera värdena av elementen i listan.

Det slutliga resultatet är att vi får en lista som har *m* element där varje element är en lista av nollor med längden *n*. D.v.s. en **matris** med formen $m\times n$.

### Implementation

Implementationen av matristransponering kan se ut så här:

```python
def transpose(A):
    # 1. Definiera dimensioner av A
    
    # Antalet rader i A
    m = len(A)
    # Antalet kolumner i A
    # Den här if-satsen är nödvändig för att undvika en IndexError om det
    # inte finns några rader när vi ska kolla längden av första raden
    n = len(A[0]) if len(A) > 0 else 0
    
    # 2. Kontrollera att matriserna är av godtycklig typ om applicerbart
    # Alla matriser har ett transponat
    
    # 3. Skapa en tom matris C av typen n×m (n rader och m kolumner)
    C = [[0]*m for _ in range(n)]
    
    # 4. Iterera genom varje rad i C
    for i in range(n):
        # 4.1. Iterera genom varje element på raden
        for j in range(m):
            # Beräkna värdet på elementet
            C[i][j] = A[j][i]
    
    return C
```

## Powers

I `powers` skapar vi en ny matris $C$ från en **lista** $A$, ett tal $a$ vilket är vår *minsta potens*, och ett tal $b$ som är vår *största potens*. Typen av den resulterande matrisen är $\lvert A \rvert\times b-a+1$ och ett element i matrisen definieras enligt:

$$
C_{ij}=A_{i}^{a+j-1}
$$

Där det första elementet är $C_{11}$.

### Implementation

För att implementera funktionen använder vi samma algoritm som ovan med några små justeringar:

```python
def powers(A, a, b):
    # 1. Definiera dimensioner av A
    
    # Antalet element i A
    m = len(A)
    
    # Antalet kolumner i den resulterande matrisen C
    n = b-a+1
    
    # 2. Kontrollera att matriserna är av godtycklig typ om applicerbart
    # Vi behöver inte göra någon kontroll, eventuellt att a<=b men vi
    # antar att det är inte nödvändigt
    
    # 3. Skapa en tom matris C av typen m×n (m rader och n kolumner)
    C = [[0]*n for _ in range(m)]
    
    # 4. Iterera genom varje rad i C
    for i in range(m):
        # 4.1. Iterera genom varje element på raden
        for j in range(n):
            # Beräkna värdet på elementet
            C[i][j] = A[i]**(a+j) # Inte j-1 eftersom j räknar från 0
    
    return C
```

## Multiplikation av matriser

### Skalärprodukten

För att multiplicera två matriser behöver vi först bekanta oss med begreppet *skalärprodukt*. Om `a` och `b` är två listor av samma längd $n$ är **skalärprodukten** $a\cdot b$ samma som `a[0]*b[0] + a[1]*b[1] +... + a[n]*b[n]`.

### Hur fungerar matrismultiplikation?

I produkten av en matrismultiplikation är värdet på ett element $C_{ij}$ en skalärprodukt mellan raden $i$ i matrisen $A$ och kolumnen $j$ i matrisen $B$.

Eftersom listorna i en skalärprodukt måste vara av samma längd kan produkten mellan matriserna $A$ och $B$ bara vara definierad **om antalet kolumner i matris $A$ är samma som antalet rader i matris $B$**. Vi kallar denna gemensamma längd för $n$. Det kan även uttryckas som att $A$ har typen $m\times n$ och $B$ har typen $n\times p$.

### Implementation

En implementationen av matrismultiplikation med vår [[02 - Areas/School/Courses/TDA548 - Grundläggande programmering/Matrismatte för labb 2#Algoritmen för matrisoperationer\|algoritm från ovan]] kan se ut så här:

```python
def matmul(A, B):
	# 1. Definiera dimensioner av A och B
	
	# Antalet rader i A
    m = len(A)
    # Antalet kolumner i A och rader i B
    n = len(A[0]) if len(A) > 0 else 0
    # Antalet kolumner i B
    p = len(B[0]) if len(B) > 0 else 0
	
    # 2. Kontrollera att matriserna är av godtycklig typ
    #    (kolumner i A == rader i B)
    if n != len(B):
        pass # Hantera fallet då matriserna inte kan multipliceras
    
    # 3. Skapa en tom matris C av typen m×p (m rader och p kolumner)
    C = [[0]*p for _ in range(m)]
    
    # 4. Iterera genom varje rad i C
    for i in range(m):
        # 4.1. Iterera genom varje element på raden
        for j in range(p):
            # Beräkna skalärprodukten
            scalar = 0
            for k in range(n):
                scalar += A[i][k] * B[k][j]
	        
			C[i][j] = scalar
    
    return C
```
