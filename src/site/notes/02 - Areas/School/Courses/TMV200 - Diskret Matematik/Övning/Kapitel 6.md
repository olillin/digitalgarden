---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Övning/Kapitel 6.md","permalink":"/TMV200 - Diskret Matematik/Övning/Kapitel 6/"}
---

6.12.

(a) Hur många sjusiffriga tal, d.v.s. heltal $n$ $10^6\leq n<10^7$, finns det som innehåller exakt 2 ettor, exakt 1 trea och exakt 3 åttor?

> Det finns totalt $9*10^6= 9.000.000$ sjusiffriga tal. Vi har bara 9 val till första siffran eftersom om talet började på 0 skulle det inte vara sjusiffrigt.
> 
> Utav de 7 siffrorna är 6 av dessa redan bestämda utan plats.
> Eftersom det inte får finnas fler av dessa 3 siffror har vi endast 7 val kvar för den sista siffran (6 om det är första siffran).
> 
> Vi skriver vårt sjusiffriga tal med formen: *ABCDEFG* där *A–F* är våra bestämda siffror och *G* är den obestämda siffran. Hur många sådana tal finns det? Först tittar vi på de bestämda talen *A–F*: Om alla siffror var unika skulle det finnas $_{6}P_{6}=\frac{6!}{(6-6)!}=6!= 720$ sätt. Men eftersom det finns dubbletter av siffrorna 1 och 8 måste dessa tas bort.
> 
> Siffran *888DEFG* förekommer exempelvis $_{3}P_{3}=3!= 6$ gånger när alla siffror behandlas som unika. Därför behöver vi dividera med $6$ för att ta bort dubbletterna av 8.
> 
> $\frac{720}{6}= 120$
> 
> Detsamma gäller för 1:orna vilket det finns 2 av. Vi dividerar med $_{2}P_{2}=2!=2$:
> 
> $\frac{120}{2}= 60$
> 
> Det finns alltså 60 sätt att arrangera våra bestämda siffror *A–F*.
> 
> För varje av dessa kan *G* anta 7 värden: $\{ 0,2,4,5,6,7,9 \}$. Enligt multiplikationsprincipen finns det alltså $60*7= 420$ sjusiffriga tal *ABCDEFG*.
> 
> Det finns totalt 6 platser där *G* har 7 val, och 1 där *G* har 6 val.
> 
> Därför finns det totalt $6*60*7+1*60*6= 2880$ sjusiffriga tal som innehåller exakt 2 ettor, exakt 1 trea och exakt 3 åttor.  

(b) Hur många av dessa är udda?

> Ett tal är udda om den sista siffran är 1, 3, 5, 7 eller 9.
> 
> Vi tar exemplet av *ABCDEFG* igen:
> Här kan den sista siffran *G* anta 7 värden $\{ 0,2,4,5,6,7,9 \}$ varav 3 av dessa skulle göra att siffran är udda.
> 
> Det finns alltså 60 sätt att arrangera siffrorna *A—F* och 3 sätt att bestämma siffran *G* så talet är udda. D.v.s. $60*3= 180$ sätt.
> 
> Det finns $420*5= 2100$ tal som *ABCDEGF* där *G* är någonstans i mitten av talet kan den sista siffran anta 6 värden med dubbletter: $\{ 1,1,3,8,8,8 \}$ varav 3 av dessa skulle göra att siffran är udda, d.v.s. hälften. Vi dividerar därför bort hälften av dessa tal och får $\frac{2100}{2}= 1050$ udda tal.
> 
> Det finns $6*60= 360$ tal som *GABCDEF* där *G* är i början på talet där det endast finns 6 val till *G*. Enligt samma logik som ovan dividerar vi bort hälften av dessa och får $\frac{360}{2}= 180$ sätt som ett tal *GABCDEF* är udda.
> 
> Adderar vi alla dessa får vi $180+1050+180= 1410$ totalt udda sjusiffriga tal.
****