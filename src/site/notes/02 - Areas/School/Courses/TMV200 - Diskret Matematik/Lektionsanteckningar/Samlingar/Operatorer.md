---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Operatorer.md","permalink":"/TMV200 - Diskret Matematik/Lektionsanteckningar/Samlingar/Operatorer/"}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-02/#logiska-operatorer" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Logiska operatorer

| Operator             | Notation                           | Innebörd                           | Förklaring                                                                       |
| -------------------- | ---------------------------------- | ---------------------------------- | -------------------------------------------------------------------------------- |
| Konjunktion          | $P \land Q$                        | $P$ och $Q$                        | Utsaga som är sann om och endast om både $P$ och $Q$ är sanna.                   |
| Disjunktion          | $P \lor Q$                         | $P$ eller $Q$                      | Utsaga som är sann när $P$ och/eller $Q$ är sanna.                               |
| Negation             | $\neg{P}$                          | Inte $P$                           | Utsaga som är sann när $P$ är falskt.                                            |
| Exklusiv disjunktion | $P \lor Q \land \neg{(P \land Q)}$ | $P$ eller $Q$ men inte $Q$ och $P$ | Utsaga som är sann när $P$ eller $Q$ är sanna men inte när $P$ och $Q$ är sanna. |


</div></div>



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tmv-200-diskret-matematik/lektionsanteckningar/2024-09-16/#operatorer" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## Operatorer

### Identitet (för \*)
$e\in A\text{ sådant att }e*a=a*e=a\forall a\in A$
### Invers
$\text{Antag }e\text{ är en identitet för }*\text{ på } A\text{. För }a\in A\text{, om det finns }b\in A\text{ så att }b*a=a*b=e\text{, kallas }b\text{ en invers till }a\text{.}$

Övning. Om $a$ har invers $b$, är $a$ alltid invers till $b$?

### Kommunativitet
$*\text{ är kommunativ om }a*b=b*a\text{ }\forall a,b\in A$
### Associativitet
$*\text{ är associativ om }\forall a,b,c\in A\text{, }a*(b*c)=(a*b)*c$
### Sats (3.30)

Låt $*$ vara en binär operator på en icke-tom mängd $A$. Det finns som mest en identitet för $*$ på $A$. Om $a\in A$ och $*$ är associativ har $a$ högst en invers m.a.p. $*$

#### Bevis

$e_1=e_1*e_2=e_2*e_1=e_2$

$e_1=e_2$, det kan bara finnas en identitet, V.S.B.

Antag att $a$ har två inverser, $b,c\text{ (m.a.p. }*\text{)}$. Vill visa $b=c$
$b=b*e=b*(a*c)=(b*a)*c=e*c=c$

</div></div>

