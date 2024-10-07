---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Grafteori.md","permalink":"/TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Grafteori/"}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-26/#grafteori" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Grafteori

### Vad är en graf?

En graf består av en mängd *noder* och en mängd *kanter* mellan noder.

Formellt: En graf är $G=(V,E)$
- $V$ mängden noder (vertices)
- $E$ mängden kanter (edges)

$\{ x,y \}\in E,\enspace x,y\in V$ är en kant mellan noderna $x$ och $y$

I denna kurs gäller:

- Det finns bara en möjlig kant mellan 2 noder
- En nod kan inte ha en kant med sig själv ($\{ x,y \}\not\in E$)

#### Sammanhängande graf

En graf kallas *sammanhängande* om det finns en väg mellan alla par av noder $u,v\in V$

### Vägar

En *väg* mellan två noder $u,v$ är en följd av noder $v_{0},v_{1},\dots,v_{n}$ där: 
$v_{0}=u,\enspace v_{n}=v,\enspace \{ v_{i},v_{i+1} \}\in E,\enspace i\in \{ 0,1,\dots ,n \}$

En *cykel* är en väg där ingen kant upprepas som börjar och slutar i samma nod, d.v.s. $u=v$.

En *enkel* väg är en väg utan upprepande noder.
### Isomorfa grafer

Graferna $G,\tilde{G}$ är "samma graf" om vi kan byta "namn" på noderna för att få samma mängd av kanter.

> [!Example] Formell definition
> $G$ och $\tilde{G}$ är *isomorfa* om det finns en bijektion $f:V\to \tilde{V}$ så att $\{  x,y\}\in E\iff \{ f(x),f(y) \}\in \tilde{E}$
> 
> $f$ inducerar en bijektion mellan $G$ och $\tilde{G}$.

#### Metod för att se om två grafer är isomorfa

Vi har graferna $G_{1},G_{2}$ som vi vill undersöka om de är isomorfa:

1. Börja med en nod $v_{0}$ i $G_{1}$ med ett unikt antal kanter.
2. Om det finns exakt en nod $u_{0}$ med lika många kanter i $G_{2}$ så måsta dessa vara samma nod. D.v.s. $f(v_{0})=u_{0}$

### Delgrafer

Låt $G=(V,E),\tilde{G}=(\tilde{V},\tilde{E})$ vara två grafer.
1. $\tilde{G}$ är en *delgraf*  till $G$ om $\tilde{V}\subseteq V$ och $\tilde{E} \subseteq E$
2. $\tilde{G}$ är en *inducerad delgraf* till $G$ om $\tilde{G}$ är en delgraf och om $x,y\in \tilde{V}\land\{ x,y \}\in E$ gäller $\{ x,y \}\in \tilde{E}$. D.v.s. att vi inte tar bort fler noder än nödvändigt.


</div></div>



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-30/#grafteori" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Grafteori

### Maximalt sammanhängande delgraf

En [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-26#Definitioner\|sammanhängande]] [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-26#Delgrafer\|delgraf]] $\tilde{G}=(\tilde{V},\tilde{E})$ till $G=(V,E)$, så den att för alla $\hat{V}\subseteq V:\tilde{V}\subseteq \hat{V}\subseteq V$ gäller att den [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-26#Delgrafer\|inducerade]] delgrafen för $\hat{V}$ **ej är sammanhängande**.

"Kan jag lägga till en [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-26#Vad är en graf?\|nod]] i den inducerade delgrafen utan att den slutar vara **sammanhängande**? Om jag **inte** kan det är den *maximalt sammanhängande*."

### Gradtal

För en nod $v\in V$ är $v

s *gradtal*:

$d_{v}=\text{antal kanter i G vars ena ände är i }v$
$\enspace=\text{antal noder i G länkade till v via en kant}$
$\enspace=\lvert \{ u\in V:\{ u,v \}\in E \} \rvert$

### Fullständig

En graf $G$ är *fullständig* om det finns en kant mellan varje par av noder.

Notation: $K_{n}:\text{fullständig graf på n noder}$

### Bipartit

$G=(V,E)$ kallas *bipartit* om det finns delmängder $A\subseteq V,B\subseteq V$ så att $A\cup B=V,\enspace A\cap B=\emptyset$ och så att $\forall x,y\in E:(x \in A\land y\in B)\lor(x \in B\land y\in A)$

> [!Tip] Tänk
> Om en graf är bipartit kan alla noder färgläggas med två färger så att alla kanter går från en färg till en annan.

#### Fullständigt bipartit 

En [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Grafteori#bipartit\|#bipartit]] graf $G=(V,E)$ är *fullständigt bipartit* om $\forall a\in A,\forall b\in B:\{ a,b\}\in E$.

Notation: $K_{m,n}:$ fullständigt bipartit graf med $\lvert A \rvert=m,\enspace \lvert B \rvert=n,\enspace n\geq m$

### Träd

En graf $G=(V,E)$ är kallas ett *träd* om $G$ är **sammanhängande** och inte innehåller **[[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-26#Vägar\|cykler]]**.

#### Satser

> [!example] Sats 1
> 
> $G=(V,E)$ är ett **träd** $\iff$ varje par $(v,w)\in V$ finns en unik [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-26#Vägar\|enkel]] väg mellan $v,w$.
> 
> Om det finns **två** vägar, då kan vi bilda en cykel.

> [!example] Sats 2
> $G=(V,E)$ är ett **träd** $\iff$ $G$ är **sammanhängande** och $\lvert E \rvert=\lvert V \rvert-1$


</div></div>


