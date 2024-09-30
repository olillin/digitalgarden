---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Logik.md","permalink":"/TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Logik/"}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-02/#logik" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Logik

### Exempel

#### I: Kort

En färg och form på varje kort.

Kort: Fyrkant, cirkel, gul, röd

*F: Om en cirkel på ena sidan är andra sidan gul*

Vilka kort måste vändas för att testa påståendet?

> Kontrollera cirkeln och röda kortet:
> - Vi bryr oss inte om ett gult kort har en cirkel på andra sidan
> - Därför får vi ingen information från att vända fyrkanten eller det gula kortet

#### II: Dricka

4 personer: 25 år, 16 år, öl och läsk

Vilka behöver kontrolleras för att lagen >18 år för alkohol ska efterföljas?

> Kontrollera 16 år och öl

Omskrivet påstående: *Dricka innehåller alkohol medför ålder > 18*

### Vad är logik?

- Logik handlar om hur man på ett korrekt sätt går från *antaganden* till en *slutsats*
### Utsagor

En *utsaga* är en syntaktiskt korrekt framställning (i något språk) som antingen är sann eller falsk.

*Notation*: Använder $P$, $Q$, $R$, ... för utsagor.

#### Exempel — Är dessa utsagor?

1) Nyårsafton infaller alltid en torsdag: Utsaga (F)
2) 1 + 1 = 2: Utsaga (S)
3) Göteborg är Sveriges huvudstad: Utsaga (F)
4) 51 är ett primtal: Utsaga (F)
5) Ekvationer $x^n+y^n=z^n$ har inga heltalslösningar för $n>2$: Utsaga (S)
6) Coop är öppet: Inte en utsaga, alldeles för vag

> [!note] Slutsats
> Vardagliga "påståenden" måste ofta preciseras eller ges kontekt för att vara utsagor.

#### Exempel — Notation

1) $P: \text{"2:a september är en tisdag"}$
2) $P(x): x < 100$

\2) är ett predikat: en utsaga som beror av variabel.

### Kombinationer av utsagor

Från två eller fler utsagor vill skapa nya utsagor.

#### Logiska operatorer

| Operator             | Notation                           | Innebörd                           | Förklaring                                                                       |
| -------------------- | ---------------------------------- | ---------------------------------- | -------------------------------------------------------------------------------- |
| Konjunktion          | $P \land Q$                        | $P$ och $Q$                        | Utsaga som är sann om och endast om både $P$ och $Q$ är sanna.                   |
| Disjunktion          | $P \lor Q$                         | $P$ eller $Q$                      | Utsaga som är sann när $P$ och/eller $Q$ är sanna.                               |
| Negation             | $\neg{P}$                          | Inte $P$                           | Utsaga som är sann när $P$ är falskt.                                            |
| Exklusiv disjunktion | $P \lor Q \land \neg{(P \land Q)}$ | $P$ eller $Q$ men inte $Q$ och $P$ | Utsaga som är sann när $P$ eller $Q$ är sanna men inte när $P$ och $Q$ är sanna. |


</div></div>



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-04/#logik" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Logik

### Ytterligare operationer

| Operator        | Notation              | Förklaring                | Övning                                   |
| --------------- | --------------------- | ------------------------- | ---------------------------------------- |
| Exklusivt eller | $P \oplus Q$          | XOR                       | $(P\lor{Q})\land\neg{(P\land{Q})}$       |
| Implikativa     | $P \rightarrow Q$     | $P$ implicerar/medför $Q$ | $(P\land{Q})\lor{\neg{P}}$               |
| Ekvivalens      | $P \leftrightarrow Q$ | $P$ om och endast om $Q$  | $(P\land{Q})\lor{(\neg{P}\land\neg{Q})}$ |
#### Sanningstabell

| $P$ | $Q$ | $P\oplus Q$ | $P\rightarrow Q$ | $P\leftrightarrow Q$ |
| --- | --- | ----------- | ---------------- | -------------------- |
| 1   | 1   | 0           | 1                | 1                    |
| 1   | 0   | 1           | 0                | 0                    |
| 0   | 1   | 1           | 1                | 0                    |
| 0   | 0   | 0           | 1                | 1                    |
### Prioriteringsregler

1. Parenteser
2. $\neg$
3. Allt annat

### Tautologier

En sammansatt utsaga, beroende på utsagor $P_{1}, \textellipsis, P_{n}$ sådan att den alltid är sann, oberoende av sanningsvärden för, kallas för *tautologi*.

#### Exempel

$
P \lor \neg{P}
$
$
(P\land{(P\rightarrow{Q})})\rightarrow{Q}
$

### Implikation och ekvivalens

Vi säger att *$P$ implicerar $Q$* logiskt om $P\rightarrow{Q}$ är en tautologi.

**Notation:** $P \implies{Q}$

Vi säger att $P$ är logiskt ekvivalent med $Q$ om $P \leftrightarrow{Q}$ är en tautologi.

**Notation:** $P\iff{Q}$

#### Exempel

$
\neg(P\lor Q)\iff \neg P \lor \neg Q
$

| $P$ | $Q$ | $P\lor Q$ | $\neg(P\land Q)$ | $\neg P\land\neg Q$ |
| --- | --- | --------- | ---------------- | ------------------- |
| 1   | 1   | 1         | 0                | 0                   |
| 1   | 0   | 1         | 0                | 0                   |
| 0   | 1   | 1         | 0                | 0                   |
| 0   | 0   | 0         | 1                | 1                   |
$
P\rightarrow Q\iff \neg Q \rightarrow\neg P
$
$P\rightarrow Q$ ej logiskt ekvivalent med $Q\rightarrow P$
Samma sak för $P\rightarrow Q$ och $\neg P\rightarrow\neg Q$
### Argument & Bevis

#### Logiskt argument

Ett *logiskt argument* består av ett antal ingående utsagor (hypoteser) $H_1,\textellipsis,H_n$ (som i sin tur byggs upp av utsagor $P_1,\textellipsis,P_m$) och en *slutsats* $C$.

Ett logiskt argument är *giltigt* om $C$ är sann så snart alla hypoteser är sanna.
// Ett giltigt logiskt argument är giltigt om $(H_1\land H_2\land\textellipsis\land H_n)\rightarrow C$ är en tautologi.
##### Notation 1:
$H_1$
$H_2$
$\vdots$
$H_n$
—
C

#### Matematiska bevis

Vill gå från axiom till slutsatser (matematiska satser/teorem)
**Typiskt:** Startar från tidigare etablerade satser.

##### Specialfall: Motsägelsebevis

Ett sätt att visa en slutsats $P$ är att anta att $P$ är falskt (dvs $\neg P$) och bevisa en uppenbart falskt utsaga $Q$. Använder logiska relationen:
$\neg P\rightarrow Q\iff \neg Q\rightarrow P$
###### Exempel

**Sats:** Det finns inga heltal $a,b$, sådana att $\sqrt{2}=\frac{a}{b}$

**Bevis:** Antag att satsen är falsk, dvs det finns heltal $a,b$ så att $\sqrt{2}=\frac{a}{b}$. Kan anta att största gemensamma nämnare för $a,b$ är $1$.

$
\sqrt{2}=\frac{a}{b}\implies 2=\frac{a^2}{b^2}\implies 2b^2=a$

$a$ måste vara ett jämnt tal.

$
\implies\text{det finns ett heltal m så att } a=2m
$
$
\implies a^2=(2m)^2=4m$
Sätt in ovan $2b^2=4m^2$
$
\implies b^2=2m$
$
b \text{ ett jämnt tal}\implies\text{det finns ett heltal } n \text{ så att } b=2n
$
$\implies\sqrt{2}=\frac{a}{b}=\frac{2m}{2n}=\frac{m}{n}$
$
\implies a,b\text{ har ej största gemensamma nämnare 1}\implies\text{antagandet falskt}
$
$
\implies\text{finns ej heltal }a,b\text{ så }\sqrt{2}=\frac{a}{b}
$

### Kvantifiera/kvantorer

Antag att $P(x)$ är ett predikat. Definierar kvantorerna
$\forall$ (allkvantorn) och $\exists$ (existenskvantorn)

$\forall x: P(x)$ utsaga som är sann om $P(x)$ är sann för alla $x$.

$\exists x: P(x)$ utsaga som är sann om det finns minst ett $x$ för vilket $P(x)$ är sann.

#### Exempel

1) För alla heltal $x$ gäller $x\leq5$

$P(x): x\leq5$
$u:\text{alla heltal}$
$\forall x\in\mathbb{Z}: P(x)$

2) "Det finns ett land i världen som ligger i Europa."

$x\text{ ett land i världen}, u:\text{alla länder}$
$P(x):x\text{ ligger i Europa}$
$\exists x\in u : P(x)$


</div></div>



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-05/#logik" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Logik

1) Associativitet för konjunktion:
$(p\land q)\land r\land r\iff p\land(q\land r)$

2) $p\land(q\lor r)\iff(p\land q)\lor(p\land r)$

### Logiska argument

1) 
$p$
$p\rightarrow q$
—
$q$

2) 
$q$
$p\rightarrow q$
—
$p$

### Kvantorer

$\forall x:(P(x)\land Q(x))\iff(\forall x:P(x))\land(\forall x:Q(x))$

$\exists x:(P(x)\lor Q(x))\iff(\exists x:P(x))\lor(\exists x:Q(x))$

$(\forall x:P(x))\lor(\forall x:Q(x))\implies\forall x:(P(x)\lor Q(x))$

$\exists x:(P(x)\land Q(x))\implies(\exists x:P(x))\land(\exists x:Q(x))$

#### Motexempel

$\neg(\forall x:P(x))\iff \exists x:\neg P(x)$

$\neg(\exists x:P(x))\iff\forall x:\neg P(x)$


</div></div>

