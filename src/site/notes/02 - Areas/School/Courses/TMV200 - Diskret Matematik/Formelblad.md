---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Formelblad.md","permalink":"/TMV200 - Diskret Matematik/Formelblad/"}
---

$[a]=\{b\in A:aRb\}$   $a\mid b:\text{a delar b}$   $\text{sgd}(a,b)=1\land a\mid bc\implies a\mid c$ 
Om $a$ är ett primtal och $a\nmid b$ så är $\text{sgd}(a,b)=1$

![Pasted image 20241023194014.png](/img/user/06%20-%20Resources/Attachments/Pasted%20image%2020241023194014.png)

$\mathbb{Q}:\text{Rationella tal}$   $\mathbb{R}:\text{Reella tal}$   $\emptyset:\text{Tomma mängden}$

> [!Example] Sats 7.11
> En sammanhängande graf $G$ innehåller en **Eulercykel** om och endast om alla [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-30#Gradtal\|gradtal]] i $G$ är jämna.

> [!Example] Sats 7.12
> Låt $u,v\in V,\enspace u\neq v$ vara två noder i en sammanhängande graf $G=(V,E)$. $G$ **innehåller minst en Eulerväg** från $u$ till $v$ om och endast om $d_{u}$ och $d_{v}$ är **udda** och för alla andra noder $w\in V$ gäller att $d_{w}$ är **jämnt**.

> [!example] Sats 5.22
> Den [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Formelblad#Diofantiska ekvationer\|diofantiska ekvationen]] $ax+by=c$ är lösbar om och endast om $sgd(a,b)\mid c$

| Summor                                                                                                                                                                                                                   | Kombinatorik                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------- |
| $\sum_{i=a}^{b} (A_i+B_i)=\sum_{i=a}^{b} A_i+\sum_{i=a}^{b} B_i$<br><br>$\enspace\sum_{x\in M} x=1+2+3$<br><br>$\prod_{i=1}^n a_i=a_1*a_2*\dots*a_n$<br><br>Aritmetisk summa: $\sum_{i=1}^{n} a_i=\frac{n}{2}*(a_1+a_n)$ | ${n\choose k}=\frac{n!}{k!(n-k)!}$<br>$_nP_k=\frac{n!}{(n-k)!}$ |

| Begrepp            | Förklaring                                                                                                                                   | Notation                 |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ |
| Antisymmetrisk     | $(aRb\land bRa)\implies a=b\enspace\forall a,b\in A$                                                                                         |                          |
| Associativitet     | $(a*b)*c=a*(b*c)$                                                                                                                            |                          |
| Bijektiv           | Injektiv och surjektiv                                                                                                                       |                          |
| Bipartit graf      | Graf då noder kan delas in i två grupper och alla kanter går mellan grupperna                                                                |                          |
| Diofantisk ekv.    | Bestående av och lösning med heltal i $\mathbb{Z}$                                                                                           |                          |
| Disjunktion        | "eller"                                                                                                                                      | $\lor$                   |
| Ekvivalensrelation | Reflexiv, symmetrisk och transitiv                                                                                                           |                          |
| Gradtal            | Antalet kanter som ansluter till en nod                                                                                                      | $d_{v}$                  |
| Kardinalitet       | Storleken/antalet element i en mängd                                                                                                         | $\lvert A \rvert$        |
| Konjunktion        | "och"                                                                                                                                        | $\land$                  |
| Kvantifiera        | Bind variablerna i ett predikat för att få ett sanningsvärde                                                                                 | $\forall{}$, $\exists{}$ |
| Identitet          | $e$ sådant att $a*e=a\enspace\forall{a\in A}$                                                                                                | $e$                      |
| Inducerad delgraf  | $\tilde{G}=(\tilde{V},\tilde{E})$ är inducerad delgraf till $G=(V,E)$ då $\forall{x,y\in \tilde{V}}:\{ x,y \}\in E\to\{ x,y \}\in \tilde{E}$ |                          |
| Injektiv           | Alla funktionsärden $f(x)$ är unika                                                                                                          |                          |
| Invers             | Funktion: $g$ är invers till $f$ om $f(g(x))=x$<br>Operator: $a*a^{-1}=e$ där $e:\text{identitet på A}$                                      | $f^{-1}$<br>$a^{-1}$     |
| Partiell ordning   | Reflexiv, antisymmetrisk och transitiv                                                                                                       |                          |
| Reflexiv           | $aRa\enspace\forall a\in A$                                                                                                                  |                          |
| Specificera        | Specificera variabeln i ett predikat för att få ett sanningsvärde                                                                            |                          |
| Surjektiv          | $f:A\to B,\enspace\forall{b\in B\enspace\exists{a\in A:f(a)=b}}$                                                                             |                          |
| Symmetrisk         | $aRb\implies bRa\enspace\forall a,b\in A$                                                                                                    |                          |
| Transitiv          | $(aRb\land bRc)\implies aRc\enspace\forall a,b,c\in A$                                                                                       |                          |
Blandad notation: $D_{f}$, $V_{f}$
