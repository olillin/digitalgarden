---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Relationer.md","permalink":"/TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Relationer/"}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-16/#relationer" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Relationer

### Vad är en relation?

Tidigare exempel på relationer:

- Logiska relationer: $\implies$, $\iff$
- Mängder: $\subseteq$, $=$

$A, B$ är två icke-tomma mängder. En relation från $A$ till $B$ är en delmängd $R\subseteq A\times B=\set{(a,b):a\in A,b\in B}$, Om $A=B$ säger vi att $R$ är en relation på $A$. 

För $a\in A,b\in B$, tolka $(a,b)\in R$ som att "$a$ är relaterat till $b$" enligt den regel som beskriver $R$.

#### Notation

$(a,b)\in R$ skrivs $a R b$

### Exvivalensrelationer & Partiell ordning

#### Egenskaper

3.36, 3.39, 3.48

1. Reflexiv om $\forall a\in A: a R a$
2. Symmetrisk om $a R b\implies b R a\enspace\forall a,b\in A$
3. Antisymmetrisk om $(a R b \land b R a)\implies a=b\enspace\forall a,b\in A$
4. Transitiv om $(a R b \land b R c)\implies a R c\enspace\forall a,b,c\in A$
5. Partiell ordning om $R$ är reflexiv, antisymmetrisk och transitiv
6. Ekvivalensrelation om $R$ reflexiv, symmetrisk och transitiv

> [!Warning] OBS
> En relation $R$ kan vara både symmetrisk och antisymmetrisk, en av de eller ingetdera.

> [!Note] Notera
> Relationen definierad på $\mathbb{R}\times\mathbb{R}$ av $=$ har egenskaperna 1-4.

> $\leq$ ger upphov till en partiell ordning på $\mathbb{R}$.

> $R: \text{två räta linjer är parallella}$
> $R$ är en ekvivalensrelation

> $A=\set{\text{alla städer i Europa}}$
> $xRy\iff x$ ligger i samma land som $y$
> $R$ är en ekvivalensrelation


#### Definition

För en ekvivalensrelation $R$ på $A$, för $a\in A$ definierar vi: $[a]=\{b\in A:aRb\}$
$[a]$ kallas för "$a


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-18/#relationer" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Relationer

Relationen $*$ på $A$ noteras $(A,*)$

### Partiell ordning

Noteras: $a\preceq b$ då:
$a\preceq a\enspace\forall a\in A$
$a\preceq b\implies b\preceq a\enspace\forall a,b\in A$
$(a\preceq b\land b\preceq c)\implies a\preceq c\enspace\forall a,b,c\in A$

### Total ordning

En partiell ordning blir en total ordning om: $a\preceq b\lor b\preceq a\enspace\forall a,b\in A$

Exempel: $\geq$ är en total ordning på $\mathbb{R}$


</div></div>

s ekvivalensklass" (notera $a\in[a]$, eftersom $R$ reflexiv)

I exemplet utegör länderna i Europa ekvivalensklasserna.

1. $a\in[a]$
2. $aRb\implies[a]=[b]$
3. $a$ ej relaterad till $b\implies[a]\cap[b]=\emptyset$ (betyder att ekvivalensklasserna för $R$ ger en uppdelning av $A$ i disjunkta delmängder. En partition av $A$).

</div></div>


![[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-18#Relationer\|2024-09-18#Relationer]]
