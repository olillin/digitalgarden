---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Övning/Kapitel 1.md","permalink":"/TMV200 - Diskret Matematik/Övning/Kapitel 1/"}
---

1) Konstruera fem "påståenden" som inte är utsagor i logisk mening.

- Dörren är öppen
- Maj är min favoritmånad
- Julen är lång
- Chalmerister får bra jobb
- Svenska är det bästa språket

2) Konstruera tio logiska utsagor och ange deras sanningsvärden.

- En stol går att sitta på. *S*
- Vattenmelon innehåller vatten. *S*
- Gravitation finns bara på jorden. *F*
- Det svenska ordet "här" används för att beskriva en plats. *S*
- Undertale släpptes år 2015. *S*
- Alla människor kan prata engelska. *F*
- Bra anslutningar via kollektivtrafik minskar antalet bilister. *S*
- Majoriteten av människor kan se. *S*
- Utsläpp av växthusgaser orsakar global uppvärmning. *S*
- Spotify finns som en app på telefonen. *S*

3) Betrakta följande utsagor:
	
	$p:\text{Solen skiner idag.}$	
	$q:\text{Vitsipporna står i blom.}$
	$r:\text{Det blåser sydlig vind.}$
	
	Skriv följande utsagor i ord: $p\lor q$, $p\land\neg r$, $p\land(q\lor r)$, $\neg q\lor(\neg p\land r)$. Gör sanningstabell.

| Notation                    | Ord                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------------ |
| $p\lor q$                   | Solen skiner idag eller vitsipporna står i blom.                                     |
| $p\land\neg r$              | Solen skiner idag och det blåser inte sydlig vind.                                   |
| $p\land(q\lor r)$           | Solen skiner idag och vitsipporna står i blom eller det blåser sydlig vind.          |
| $\neg q\lor(\neg p\land r)$ | Vitsipporna står inte i blom eller solen skiner inte idag och det blåser sydlig vind |

| $p$ | $q$ | $r$ | $p\lor q$ | $p\land\neg r$ | $p\land(q\lor r)$ | $\neg q\lor(\neg p\land r)$ |
| --- | --- | --- | --------- | -------------- | ----------------- | --------------------------- |
| 0   | 0   | 0   | 0         | 0              | 0                 | 1                           |
| 1   | 0   | 0   | 1         | 1              | 0                 | 1                           |
| 0   | 1   | 0   | 1         | 0              | 0                 | 0                           |
| 1   | 1   | 0   | 1         | 1              | 1                 | 0                           |
| 0   | 0   | 1   | 0         | 0              | 0                 | 1                           |
| 1   | 0   | 1   | 1         | 0              | 1                 | 1                           |
| 0   | 1   | 1   | 1         | 0              | 0                 | 1                           |
| 1   | 1   | 1   | 1         | 0              | 1                 | 0                           |

4) Skilj ut delpåståendena i följande utsagor, skriv på symbolisk logisk form och gör en sanningstabell:
	1) Om bilen startar och du inte bråkar så åker vi till Liseberg och du slipper städa ditt rum.

$p: \text{Bilen startar}$
$q: \text{Du bråkar}$
$r: \text{Vi åker till Liseberg}$	
$s: \text{Du behöver städa ditt rum}$

$p\land\neg q\rightarrow r\land\neg s$

	2) Om det regnar eller haglar, så stannar jag antingen inne eller tar med
	   mig paraplyt.

$p: \text{Det regnar}$	
$q: \text{Det haglar}$
$r: \text{Jag stannar inne}$	
$s: \text{Jag tar med mig paraplyt}$

$p\lor q\rightarrow r\lor s$

5) Konstruera fyra par av logiska utsagor och avgör om logisk ekvivalens föreligger eller ej.

$p: \text{}$

6) Skriv följande argument på symbolisk logisk form och avgör om det är giltigt: "Idag ska jag vara snäll eller göra min läxa. Om jag är snäll blir mamma glad. Om mamma blir glad får jag godis. Om jag gör min läxa blir pappa glad. Alltså får jag godis idag."

$p: \text{Idag ska jag vara snäll.}$
$q: \text{Idag ska jag göra min läxa.}$
$r: \text{Mamma blir glad.}$
$s: \text{Pappa blir glad.}$
$t: \text{Jag får godis.}$

$p\lor q$
$p\rightarrow r$
$q\rightarrow s$
$r\rightarrow t$
—
$t$

Argumentet är inte giltigt, $p\lor q$ kan vara sant utan att $p$ är sant och $p$ måste vara sant för att $t$ ska vara sant.

7) Avgör vilka av följande logiska argument som är giltiga:
	
	a) 
	$s\lor t$
	$t\rightarrow r$
	$s\rightarrow w$
	—
	$r\rightarrow w$
Ogiltigt
	b)
	$p\rightarrow q$
	$q\rightarrow r$
	$r$
	—
	$p$
Ogiltigt
	c)
	$p\rightarrow q$
	$(\neg q)\rightarrow(\neg s)$
	$s\rightarrow t$
	$t\lor q$
	—
	$p\lor s$

| $p$ | $q$ | $s$ | $t$ | $p\rightarrow q$ | $(\neg q)\rightarrow(\neg s)$ | $s\rightarrow t$ | $t\lor q$ | $p\lor s$ |
| --- | --- | --- | --- | ---------------- | ----------------------------- | ---------------- | --------- | --------- |
| 0   | 0   | 0   | 0   | 1                | 1                             | 1                | 0         | 0         |
| 1   | 0   | 0   | 0   | 0                | 1                             | 1                | 0         | 1         |
| 0   | 1   | 0   | 0   | ==1==            | ==1==                         | ==1==            | ==1==     | ==0==     |
| 1   | 1   | 0   | 0   | 1                | 1                             | 1                | 1         | 1         |
| 0   | 0   | 1   | 0   | 1                | 0                             | 0                | 0         | 1         |
| 1   | 0   | 1   | 0   | 0                | 0                             | 0                | 0         | 1         |
| 0   | 1   | 1   | 0   | 1                | 1                             | 0                | 1         | 1         |
| 1   | 1   | 1   | 0   | 1                | 1                             | 0                | 1         | 1         |
| 0   | 0   | 0   | 1   | 1                | 1                             | 1                | 1         | 0         |
| 1   | 0   | 0   | 1   | 0                | 1                             | 1                | 1         | 1         |
| 0   | 1   | 0   | 1   | ==1==            | ==1==                         | ==1==            | ==1==     | ==0==     |
| 1   | 1   | 0   | 1   | 1                | 1                             | 1                | 1         | 1         |
| 0   | 0   | 1   | 1   | 1                | 0                             | 1                | 1         | 1         |
| 1   | 0   | 1   | 1   | 0                | 0                             | 1                | 1         | 1         |
| 0   | 1   | 1   | 1   | 1                | 1                             | 1                | 1         | 1         |
| 1   | 1   | 1   | 1   | 1                | 1                             | 1                | 1         | 1         |

Argumentet är ogiltigt
	d)
	$(\neg p)\lor q$
	$r\lor\neg q$
	$p$
	$s$
	—
	$r\lor s$

Argumentet är giltigt, däremot är de första tre utsagorna onödiga
	e)
	$\neg(s\land t)$
	$(\neg w)\rightarrow t$
	—
	$s\rightarrow w$


| $s$ | $t$ | $w$ | $\neg(s\land t)$ | $(\neg w)\rightarrow t$ | $s\rightarrow w$ |
| --- | --- | --- | ---------------- | ----------------------- | ---------------- |
| 0   | 0   | 0   | 1                | 0                       | 1                |
| 1   | 0   | 0   | 1                | 0                       | 0                |
| 0   | 1   | 0   | 1                | 1                       | 1                |
| 1   | 1   | 0   | 0                | 1                       | 0                |
| 0   | 0   | 1   | 1                | 1                       | 1                |
| 1   | 0   | 1   | 1                | 1                       | 1                |
| 0   | 1   | 1   | 1                | 1                       | 1                |
| 1   | 1   | 1   | 0                | 1                       | 1                |
Giltigt