---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Kombinatorik.md","permalink":"/TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Kombinatorik/"}
---



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-23/#kombinatorik" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Kombinatorik

${n\choose k}=\frac{n!}{k!(n-k)!}$

$_nP_k=\frac{n!}{(n-k)!}$


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-25/#kombinatorik" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Kombinatorik

### Binomialsatsen

För $n\in\mathbb{Z}_+$, $x,y$ variabler

$(x+y)^n=\sum^{n}_{k=0}{n\choose k}x^{k}*y^{n-k}$

Exempel: 

$(2+3)^2=\sum^{2}_{k=0}{2\choose k}2^k*3^{2-k}={2\choose 0}2^0*3^{2-0} + {2\choose 1}2^1*3^{2-1} + {2\choose 2}2^2*3^{2-2} = 9+12+4 = 25$

### Hjälpsats

${{n+1}\choose{k+1}}={n\choose k}+{n\choose k+1}$

För $n\in\mathbb{Z}_+$ och $p\in (0,1)$ gäller $\sum^{n}_{k=0}{n\choose k}p^k*(1-p)^{n-k}=(p+1(1-p))^n=1^n=1$

Beräkna för $n\in\mathbb{Z}_+$, $\sum^{n}_{k=0}{n\choose k}$

**Alt 1**: Sätt $x=y=1$ i binomialsatsen:

$(1+1)^n=\sum^{n}_{k=0}{n\choose k}1^k*1^{n-k}=\sum^{n}_{k=0}{n\choose k}$

### Exempel:

På hur många sätt kan 7 lika bollar placeras i 4 boxar?

> [!Note] Enklare exempel
> Om ej lika (de alla går att särskilja) finns det $4^7$ sätt. För varje boll finns det 4 val av lådor och vi väljer 7 gånger för 7 bollar.

> [!Success] Lösning
> För lika bollar tänk på bollarna i en följd. 
> Att dela in de i 4 lådor är detsamma som att bestämma 3 avgränsningar mellan bollarna:
>   ••|•••|••|
>   
> Det är ekvivalent med att placera ut 10 objekt (7 bollar och 3 avgränsningar) vilket ges av ${10\choose 3}=120$

Allmänt gäller att $n$ lika objekt kan fördelas i $k$ "lådor" på $n+k-1\choose k-1$ sätt.

### Lådprincipen

$n$ saker ska placeras i $m$ "lådor". Om $n>m$ måste det finnas minst en låda med fler än 1 sak i.

#### Formellt

$L=\text{"mängden av lådor som vi har"}$
$n\in \mathbb{Z}\land n<|L|$
$\text{"n saker delas in i lådorna L"}\implies \exists{l}\in L,\enspace\text{"saker i l"}>1$

### Inklusion-exklusion principen

$A_{i}\cap A_{j}=\emptyset\enspace\forall{i,j}\in \mathbb{N}\implies \left\lvert  \bigcup_{i=1}^{n}A_{1} \right\rvert =\sum_{i=1}^{n} \lvert A_{1} \rvert $

$\left\lvert  \bigcup_{i=1}^{n}A_{i}  \right\rvert=\sum_{i=1}^{n}\lvert A_{i} \rvert -\sum_{i,j;i<j}  \lvert A_{i}\cap A_{j} \rvert +\sum_{i,j,k;i<j<k} \lvert A_{i}\cap A_{j}\cap A_{k} \rvert-\dots \pm \sum_{i,} \dots$


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-26/#kombinatorik" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Kombinatorik

### Exempel: Mängden funktioner

$A=\{ 1,2,3,4,5,6 \},\enspace B=\{ a,b,c \}$

Hur många [[02 - Areas/School/Courses/TMV200 - Diskret Matematik/Lektionsanteckningar/2024-09-11#Funktioner\|surjektiva]] funktioner $f:A\to B$ finns det?

Antalet funktioner $A$ till $B$: $C=\{ f:A\to B \}$
Antalet surjektiva funktioner $A$ till $B$: $D$

$\lvert C \rvert=3^6$
$\lvert D \rvert=\lvert C \rvert-(\lvert C_{a} \rvert+\lvert C_{b} \rvert+\lvert C_{c} \rvert-\lvert C_{a}\cap C_{b} \rvert-\lvert C_{b}\cap C_{c} \rvert-\lvert C_{a}\cap C_{c} \rvert+\lvert C_{a}\cap C_{b}\cap C_{c} \rvert)$
$\enspace=3^6-3*2^6-3*1+0= 540$

#### Generalisering

Hur många funktioner från $A$ till $B$ finns det om $\lvert A \rvert=n,\enspace\lvert B \rvert=m,\enspace m<n$
$C_{i}=\{ f:A\to B,\enspace\nexists{x \in A}\text{ där }f(x)=B_{i} \}$
$\lvert D \rvert=\lvert C \rvert-\left\lvert  \bigcup_{i=1}^{m} C_{i} \right\rvert$

$\lvert C \rvert =m^n$

$\left\lvert  \bigcup_{i=1}^{m} C_{i} \right\rvert=\left\lvert  \bigcup_{i=1}^{n}A_{i}  \right\rvert=\sum_{i=1}^{n}\lvert A_{i} \rvert -\sum_{i,j;i<j}  \lvert A_{i}\cap A_{j} \rvert +\sum_{i,j,k;i<j<k} \lvert A_{i}\cap A_{j}\cap A_{k} \rvert-\dots \pm \sum_{i,} \dots$
$\enspace=\sum_{i=1}^{m}(-1)^{(i+1)}(m-i)^n$



$\lvert D_{1} \rvert=\sum_{i=0}^{m}(-1)^{i}(m-i)^n$
$\lvert D_{2} \rvert=\sum_{i=0}^{m}(-1)^{i}{m\choose i+1}(m-i)^n$

##### Test 1:
> $n=6,\enspace m=3$
> $\lvert D_{1} \rvert=\sum_{i=0}^{3}(-1)^{i}(3-i)^6$
> $\enspace=(-1)^{0}(3-0)^6+(-1)^{1}(3-1)^6+(-1)^{2}(3-2)^6+(-1)^{3}(3-3)^6$
> $\enspace=3^6-2^6+1^6-0^6$
> $\enspace=729-64+6-0=671$❌
> 
> $|D_{2}|=\sum_{i=0}^{3}(-1)^i{3\choose{i+1}}(3-i)^6$
> $\enspace=(-1)^0{3\choose{0+1}}(3-0)^6+(-1)^1{3\choose{1+1}}(3-1)^6+(-1)^2{3\choose{2+1}}(3-2)^6+(-1)^3{3\choose{3+1}}(3-3)^6$
> $\enspace={3\choose{1}}3^6-{3\choose{2}}2^6+{3\choose{3}}1^6-{3\choose{4}}0^6$
> $\enspace=3*729-3*64+1*1-0*0=1996$❌


$\lvert D_{3} \rvert=m^n+\sum_{i=1}^{m}(-1)^{i}{m\choose i}(m-i)^n$

##### Test 2
> $n=6,\enspace m=3$
> 
> $|D_{3}|=3^6+\sum_{i=1}^{3}(-1)^i{3\choose{i}}(3-i)^6$
> $\enspace=3^6-(-1)^1{3\choose{1}}(3-1)^6+(-1)^2{3\choose{2}}(3-2)^6+(-1)^3{3\choose{3}}(3-3)^6$
> $\enspace=3^6-{3\choose{2}}2^6+{3\choose{3}}1^6-{3\choose{4}}0^6$
> $\enspace=729-3*64+3*1-1*0$
> $\enspace=540$✔

##### Test 3
> $n=2,\enspace m=2$
> 
> $\lvert D \rvert=2^2+\sum_{i=1}^{2}(-1)^{i}{2\choose i}(2-i)^2$
> $\enspace=4+(-1)^{1}{2\choose 1}(2-1)^2+(-1)^{2}{2\choose 2}(2-2)^2$
> $\enspace=4-2(1)^2+{1}(0)^2$
> $\enspace=4-2+0$
> $\enspace=2$✔

> [!check] Svar
> 
> Antalet funktioner $A\to B$: $C$
> Antalet surjektiva funktioner $A\to B$: $D$
> 
> $n=\lvert A \rvert$
> $m=\lvert B \rvert$
> 
> $m<n$
> 
> $\lvert C \rvert=m^n$
> 
> $C_{i}=\{ f:A\to B,\enspace\nexists{x \in A}\text{ där }f(x)=B_{i} \}$
> 
$\lvert D \rvert=\lvert C \rvert-\left\lvert  \bigcup_{i=1}^{m} C_{i} \right\rvert$
> 
> $\lvert D \rvert=m^n+\sum_{i=1}^{m}(-1)^{i}{m\choose i}(m-i)^n$


</div></div>
