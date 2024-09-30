---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Formelblad.md","permalink":"/TMV200 - Diskret Matematik/Formelblad/"}
---

## Logik

### Operatorer

| Operator             | Notation              | Innebörd                                                                  |
| -------------------- | --------------------- | ------------------------------------------------------------------------- |
| Konjunktion          | $P \land Q$           | $P$ och $Q$                                                               |
| Disjunktion          | $P \lor Q$            | $P$ eller $Q$                                                             |
| Negation             | $\neg{P}$             | Inte $P$                                                                  |
| Exklusiv disjunktion | $P \oplus Q$          | $P$ eller $Q$ men inte $Q$ och $P$ AKA $P \lor Q \land \neg{(P \land Q)}$ |
| Implikation          | $P \rightarrow Q$     | $P$ implicerar/medför $Q$, om $P$ då $Q$                                  |
| Ekvivalens           | $P \leftrightarrow Q$ | $P$ om och endast om $Q$                                                  
#### Prioriteringsregler

1. Parenteser
2. $\neg$
3. Allt annat

### Specialfall

Motsägelsebevis: $\neg P\rightarrow Q\iff \neg Q\rightarrow P$

## Mängdlära


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-05/#saerskilda-maengder" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



### Särskilda mängder

| Notation             | Beskrivning              | Exempel                                            |
| -------------------- | ------------------------ | -------------------------------------------------- |
| $\mathbb{N}$         | Naturliga tal            | $\set{0?,1,2,3,\dots}$ (0 är ibland med)           |
| $\mathbb{Z}^+$       | Positiva heltal          | $\set{1,2,3,\dots}$                                |
| $\mathbb{N}_0$       | Naturliga tal med 0      | $\set{0,1,2,\dots}$                                |
| $\mathbb{Z}$         | Heltal                   | $\set{-1,0,1,\dots}$                               |
| $\mathbb{Q}$         | Rationella tal           | $\set{\frac{1}{2},\frac{2}{3},-\frac{3}{2},\dots}$ |
| $\mathbb{R}$         | Reella tal               | $\set{\pi,-2,\tau,e,\frac{1}{2},\dots}$            |
| $\mathbb{R}_{\geq0}$ | Icke-negativa reella tal | $\set{\pi,\tau,e,\frac{1}{2},\dots}$               |
| $\mathbb{C}$         | Komplexa tal             | $\set{(3+2i),(5-i),(7+8i),\dots}$                  |
| $\emptyset$          | Tomma mängden            | $\set{}$                                           |

</div></div>


## Funktioner

Injektiv om $x,y\in A,x\neq y\implies f(x)\neq f(y)$
Surjektiv om $f(A)=B;\forall b\in B\exists a\in A:f(a)=b$

### Invers

Om och endast om en funktion $f$ är bijektiv då har $f$ en *invers*: en funktion $g:B\rightarrow A$ som ges av: $f(x)=y\iff g(y)=x$, $g=f^{-1}$

## Operatorer

### Egenskaper

| Egenskap   | Definition                                                                                             |
| ---------- | ------------------------------------------------------------------------------------------------------ |
| Identitet  | $e\in A\text{ sådant att }e*a=a*e=a\forall a\in A$                                                     |
| Invers     | $e\text{ är en identitet för }*\text{ på } A\text{. }b\text{ är en invers till }a\text{ om }b*a=a*b=e$ |
| Kommunativ |                                                                                                        |
## Relationer

En relation $R$ på $A$ noteras som $aRb\text{ där }a,b\in A$
### Egenskaper

| Egenskap           | Definition                                             |
| ------------------ | ------------------------------------------------------ |
| Reflexiv           | $aRa\enspace\forall a\in A$                            |
| Symmetrisk         | $aRb\implies bRa\enspace\forall a,b\in A$              |
| Antisymmetrisk     | $(aRb\land bRa)\implies a=b\enspace\forall a,b\in A$   |
| Transitiv          | $(aRb\land bRc)\implies aRc\enspace\forall a,b,c\in A$ |
| Partiell ordning   | Reflexiv, antisymmetrisk och transitiv                 |
| Ekvivalensrelation | Reflexiv, symmetrisk och transitiv                     |
### Formler

$aRb\iff (a,b)\in R$
$[a]=\{b\in A:aRb\}$
$a\in[a]$
$aRb\implies[a]=[b]$
$\neg(aRb)\implies[a]\cap[b]=\emptyset$

## Summor

$\sum_{i=a}^{b} (A_i+B_i)=\sum_{i=a}^{b} A_i+\sum_{i=a}^{b} B_i$

$M=\set{1,2,3},\enspace\sum_{x\in M} x=1+2+3$

$\prod_{i=1}^n a_i=a_1*a_2*\dots*a_n$

Aritmetisk summa: $\sum_{i=1}^{n} a_i=\frac{n}{2}*(a_1+a_n)$

## Kombinatorik

${n\choose k}=\frac{n!}{k!(n-k)!}$
$_nP_k=\frac{n!}{(n-k)!}$

