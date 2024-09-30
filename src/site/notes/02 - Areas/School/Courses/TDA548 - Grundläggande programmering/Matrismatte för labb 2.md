---
{"dg-publish":true,"dg-path":"TDA548 - Grundläggande programmering/Matrismatte för labb 2.md","permalink":"/TDA548 - Grundläggande programmering/Matrismatte för labb 2/"}
---

Först och främst, det här är min egen förklaring med direkt anknytning till programmeringen där jag skummar över detaljer som inte är nödvändiga för vår implementation. Om du vill läsa mer om matrismatte är det sidor 322–337 i [diskret-matteboken](https://www.chalmersstore.se/svensk-litteratur/algebra-och-diskret-matematik.html).

## Vad är en matris?

En *matris* är en tabell av *element* som har ett antal *rader* och *kolonner*.

En matris $A=\left[\begin{array}{cc} 1 &2 &3 \\ 4 &5 &6 \end{array}\right]$ har 2 rader och 3 kolonner. Man kan även säga att $A$ är av typen $2\times3$ eller att $A$ har *dimensionen* $(2,3)$.

Ett elementet på rad $i$ och kolonn $j$ i matrisen $A$ betecknas $A_{ij}$
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
> - Ett värde i en matris på en **rad och kolonn**.

Att få ut en kolonn (`[3, 1]` eller `[2, 4]`) är inte lika enkelt som en rad eftersom en kolonn sträcker sig över flera listor. Som tur är kommer vi inte behöva det här eftersom vi endast kommer räkna på ett element i taget.

**Antalet kolonner** i matrisen är längden av våra rader. Vi tar värdet från den första raden för enkelhetens skull och får därför antalet kolonner med uttrycket: `len(matris[0])`.

För att få värdet av ett element i matrisen på rad `i` och kolonn `j` används den här koden:

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
> Lägg även märke till att matriser i Python börjar med rad och kolonn 0.

## Transponat

Ett *transponat* av en matris $A$ noteras som $A^T$ och innebär att raderna och kolonnerna byts.

T.ex:

$A=\left[\begin{array}{cc}1 &2 &3\\ 4 &5 &6\end{array}\right]$

$A^T=\left[\begin{array}{cc}1 &4\\ 2 &5\\ 3 &6\end{array}\right]$

Ett element i den transponerade matrisen definieras som $A^T_{ij}=A_{ji}$

Detta här är algoritmen vi kommer använda för våra matrisoperationer:

1. Definiera dimensionerna av våra inmatade matriser.
2. Kontrollera att de inmatade matriserna är av godtycklig typ om applicerbart.
3. Skapa en tom lista som kommer bli vår resulterande matris.
4. Skapa varje rad i matrisen med en for-loop.
    1. Skapa en tom lista för vår rad.
    2. Beräkna och lägg till värdet av varje element i raden med en for-loop.
    3. Lägg till raden i matrisen.

Implementationen av matristransponering kan se ut så här:

```python
def transpose(A):
	# 1. Definiera dimensioner av A
	
	# Antalet rader i A
    m = len(A)
    # Antalet kolonner i A
    # Den här if-satsen är nödvändig för att undvika en IndexError om det
    # inte finns några rader när vi ska kolla längden av första raden
    n = len(A[0]) if len(A) > 0 else 0
	
    # 2. Kontrollera att matriserna är av godtycklig typ om applicerbart
    # Alla matriser har ett transponat
    
    # 3. Skapa en tom lista som kommer bli vår resulterande matris
    C = []
    
    # C är av typen m×n (m rader och n kolonner)
    
    # 4. Skapa varje rad i C
    for i in range(m):
        # 4.1. Skapa en tom lista för vår rad
        row = []
        
        # 4.2. Skapa varje element på raden
        for j in range(n):
            # Beräkna och lägg till värdet på elementet i raden
            row.append(A[j][i])
        
        # 4.3. Lägg till raden i matrisen
        C.append(row)
    
    return C
```

## Multiplikation av matriser

För att multiplicera två matriser behöver vi först bekanta oss med begreppet *skalärprodukt*. Om `a` och `b` är två listor av samma längd $n$ är **skalärprodukten** $a\cdot b$ samma som `a[0]*b[0] + a[1]*b[1] + ... + a[n]*b[n]`.

I produkten av en matrismultiplikation är värdet på ett element $C_{ij}$ en skalärprodukt mellan raden $i$ i matrisen $A$ och kolumnen $j$ i matrisen $B$.

Eftersom listorna i en skalärprodukt måste vara av samma längd kan produkten mellan matriserna $A$ och $B$ bara vara definierad **om antalet kolonner i matris $A$ är samma som antalet rader i matris $B$**. Vi kallar denna gemensamma längd för $n$. Det kan även uttryckas som att $A$ har typen $m\times n$ och $B$ har typen $n\times p$.

Implementationen av detta kan se ut så här:

```python
def matmul(A, B):
	# 1. Definiera dimensioner av A och B
	
	# Antalet rader i A
    m = len(A)
    # Antalet kolonner i A och rader i B
    n = len(A[0]) if len(A) > 0 else 0
    # Antalet kolonner i B
    p = len(B[0]) if len(B) > 0 else 0
	
    # 2. Kontrollera att matriserna är av godtycklig typ
    #    (kolonner i A == rader i B)
    if n != len(B):
        pass # Hantera fallet då matriserna inte kan multipliceras
    
    # 3. Skapa en tom lista som kommer bli vår resulterande matris
    C = []
    
    # C är av typen m×p (m rader och p kolonner)
    
    # 4. Skapa varje rad i C
    for i in range(m):
        # 4.1. Skapa en tom lista för vår rad
        row = []
        
        # 4.2. Skapa varje element på raden
        for j in range(p):
            # Beräkna och lägg till värdet på elementet i raden
            
            # Beräkna skalärprodukten
            scalar = 0
            for k in range(n):
                scalar += A[i][k] * B[k][j]
	        
			row.append(scalar)
        
        # 4.3. Lägg till raden i matrisen
        C.append(row)
    
    return C
```
