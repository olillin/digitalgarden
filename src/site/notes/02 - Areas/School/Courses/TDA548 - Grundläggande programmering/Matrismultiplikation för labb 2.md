---
{"dg-publish":true,"dg-path":"TDA548 - Grundläggande programmering/Matrismultiplikation för labb 2.md","permalink":"/TDA548 - Grundläggande programmering/Matrismultiplikation för labb 2/"}
---

Först och främst, om du vill läsa mer om matten bakom matrismultiplikation är det sidor 322—329 i matteboken.

Det här är min förklaring med direkt mer anknytning till programmeringen.

## Matriser inom programmering

En matris är en tabell av siffror som har ett antal rader och kolonner. I Python representerar vi detta som en lista av listor av tal:

```python
matris = [[3, 2],
          [1, 4]]
```

I detta exempel är antalet rader i matrisen längden av den omgivande listan `{python}matris` och antalet kolonner längden av den första listan `{python}matris[0]`.
För att hitta värdet av ett element i matrisen på rad `i` och kolonn `j` används den här koden:

```python
i = 0
j = 1

element = matris[i][j]
print(element) # Ger oss värdet 2
```

## Addition av matriser

Innan vi börjar med multiplikation gör vi ett enklare exempel, addition.
För att summan av två matriser ska vara definierad krävs det att matriserna är av samma *typ*, d.v.s. att de har samma antal rader och kolonner.
Addition av matriser görs så att varje element adderas med element på samma rad och kolonn:

```python
def matadd(A, B):
    if len(A) == 0 and len(B) == 0:
	    # Matriserna är tomma och vi behöver inte göra några beräkningar
        return []
    
	# Kolla om matriserna är av samma typ
	if len(A) != len(B) or len(A[0]) != len(B[0]):
		raise Exception("Matriserna är av olika typer")
	
	# Vi skapar en tom lista som kommer bli vår resulterande matris
	C = []
	
	# Iterera för varje rad
	for i in range(len(A)):
	    # Skapa den nya raden
	    rad = []
	    
	    # Iterera för varje element i raden
	    for j in range(len(A[0])):
		    # Lägg till det nya elementet i raden
		    rad.append(A[i][j] + B[i][j])
		
		# Lägg till den färdiga raden i matrisen
		C.append(rad)
	
	return C
```

## Multiplikation av matriser

Matrismultiplikation är något svårare och den resulterande. Kravet för att multiplikationen ska vara definierad är att antalet kolonner i matris A är samma som antalet rader i matris B, vi kallar denna gemensamma dimension för `{python}n`.

