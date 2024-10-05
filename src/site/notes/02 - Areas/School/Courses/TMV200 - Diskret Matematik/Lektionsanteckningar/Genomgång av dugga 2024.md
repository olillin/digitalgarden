---
{"dg-publish":true,"dg-path":"TMV200 - Diskret Matematik/Lektionsanteckningar/Genomgång av dugga 2024.md","permalink":"/TMV200 - Diskret Matematik/Lektionsanteckningar/Genomgång av dugga 2024/"}
---


## 1.

> Skriv påståendena "Alla Volvo är röda" och "Det finns röda BMW" på predikatlogisk form. Glöm inte att definiera lämpligt universum.

**Varför är universum viktigt?**
Ett predikat är en funktion och funktioner behöver en definitionsmängd

### Lösning

Sätt $u=\text{"alla bilar"}$

Definiera, för $x \in u$:
  $V(x): x\text{ är en Volvo}$
  $B(x): x\text{ är en BMW}$
  $R(x): x\text{ är röd}$

$\forall{x \in u:V(x)\implies R(x)}$
$\exists{x \in u:B(x)\land R(x)}$

## 2.

> Definiera en talföljd $F(n),n\geq1$ ett heltal, genom
>
> $$

\begin{cases}
F(1)=1\\
F(n)=(2n-1)F(n-1),\enspace n\geq2
\end{cases}

$$
> Visa att, för alla heltal $n\geq1$,
> $$F(n)=\frac{(2n)!}{2^{n}n!}$$

### Lösning

> [!tip] Tip från Pierre
> Tänk igenom vilken metod man ska använda för att lösa en uppgift innan man börjar räkna så kör man inte fast i något hörn.

Induktionsbevis:

Basfallet: $n=1:F(1)=1,\frac{(2*1)!}{2^11!}=1$
Basfallet gäller

Antag att påståendet gäller för något $m$
Betrakta påståendet $m+1$:

$F(m+1)=(2(m+1)-1)F((m+1)-1)$
$\enspace=(2m+2-1)F(m)$
$\enspace=(2m+1)F(m)$

$\text{Induktionsantagande}=(2m+1)\frac{(2m)!}{2^mm!}=\frac{(2m+1)!}{2^mm!}$

Har $F(m+1)=\frac{(2m+1)!}{2^mm!}=\frac{2(m+1)}{2(m+1)}\cdot\frac{(2m+1)!}{2^mm!}=\frac{(2m+2)!}{2^{m+1}(m+1)!}=\frac{(2(m+1))!}{2^{m+1}(m+1)!}$

Från induktionsprincipen fås att $F(n)=\frac{(2n)!}{2^nn!}\enspace\forall{n\geq1}$

## 3.

> Rita två grafer som bägge har 5 noder, innehåller minst en triangel (en cykel med längd 3) men ej är isomorfa. Motivera varför de ej är isomorfa.

Det är inte nödvändigt att bevisa att det inte finns en bijektion.

**Exempelvis:**
I den ena grafen har jag två noder som som inte är sammankopplade till triangeln men i den andra är de kopplade.

<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="Dugga_2024_uppgift_3_24-10-03excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.1.4","elements":[{"id":"NfOsDmf42FpujQ9VKqMQq","type":"line","x":-301.25,"y":-84.9609375,"width":159,"height":115.5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":237127106,"version":57,"versionNonce":1019679006,"isDeleted":false,"boundElements":null,"updated":1727963302038,"link":null,"locked":false,"points":[[0,0],[82,-102.5],[159,13],[0,0]],"lastCommittedPoint":[0.5,-1.5],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"vDy64x2WArXae2lEJuPNx","type":"line","x":-264.25,"y":-32.9609375,"width":98,"height":13.5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1285574530,"version":143,"versionNonce":1025638622,"isDeleted":false,"boundElements":null,"updated":1727963308540,"link":null,"locked":false,"points":[[0,0],[98,13.5]],"lastCommittedPoint":[98,13.5],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"Rvo2rd41","type":"text","x":-295.75,"y":-233.9609375,"width":17.959991455078125,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":648143198,"version":3,"versionNonce":736523010,"isDeleted":false,"boundElements":null,"updated":1727963313031,"link":null,"locked":false,"text":"A:","rawText":"A:","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"A:","lineHeight":1.25},{"id":"JvmmgwkB","type":"text","x":-50.75,"y":-234.4609375,"width":19.379989624023438,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":1431257694,"version":17,"versionNonce":775702238,"isDeleted":false,"boundElements":null,"updated":1727963317694,"link":null,"locked":false,"text":"B:","rawText":"B:","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"B:","lineHeight":1.25},{"id":"Owo_u74ZhogIpde1wKzjb","type":"line","x":25.75,"y":-72.9609375,"width":149.5,"height":127,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1583523678,"version":65,"versionNonce":1448377794,"isDeleted":false,"boundElements":null,"updated":1727963322713,"link":null,"locked":false,"points":[[0,0],[48.5,-121],[149.5,6],[0,0]],"lastCommittedPoint":[2,1.5],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"Y4ZG9QKeSp_lKdKZWURaF","type":"line","x":24.75,"y":-71.4609375,"width":139,"height":102,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":687699266,"version":105,"versionNonce":1663186334,"isDeleted":false,"boundElements":null,"updated":1727963328122,"link":null,"locked":false,"points":[[0,0],[26.5,96.5],[139,102]],"lastCommittedPoint":[139,102],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"1yu6yjEOaO8JlqDhNPIWJ","type":"line","x":-199.25,"y":-36.4609375,"width":148,"height":5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1100243586,"version":19,"versionNonce":388323394,"isDeleted":true,"boundElements":null,"updated":1727963100886,"link":null,"locked":false,"points":[[0,0],[148,5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"hcvtYLxcdOxDbLbvUINjD","type":"line","x":-172.75,"y":-35.9609375,"width":163.5,"height":101,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":118816770,"version":112,"versionNonce":679980802,"isDeleted":true,"boundElements":null,"updated":1727963119627,"link":null,"locked":false,"points":[[0,0],[163.5,14],[99.5,-87],[0,0]],"lastCommittedPoint":[-2.5,-0.5],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"TuE3nM_XcVc3f-HMuKujo","type":"line","x":-138.25,"y":38.5390625,"width":84.5,"height":6,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":772904222,"version":147,"versionNonce":42699166,"isDeleted":true,"boundElements":null,"updated":1727963118247,"link":null,"locked":false,"points":[[0,0],[84.5,6]],"lastCommittedPoint":[84.5,6],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"BniOWYhAjGUa2Wr6799fV","type":"diamond","x":-240.75,"y":-136.4609375,"width":221.5,"height":232,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":384671966,"version":39,"versionNonce":1651291842,"isDeleted":true,"boundElements":null,"updated":1727963297824,"link":null,"locked":false},{"id":"mUIYziI_MbX8m9iSIfPSL","type":"line","x":-238.75,"y":-18.4609375,"width":216,"height":1.5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":411161886,"version":39,"versionNonce":1357942366,"isDeleted":true,"boundElements":null,"updated":1727963297824,"link":null,"locked":false,"points":[[0,0],[216,1.5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"XB-SdQB2gblWRFjmYO3y9","type":"line","x":-131.25,"y":-129.9609375,"width":2.5,"height":86,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":2047181150,"version":21,"versionNonce":1592561282,"isDeleted":true,"boundElements":null,"updated":1727963297824,"link":null,"locked":false,"points":[[0,0],[2.5,-86]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"ehq4k2HAdh76myUCiJRPc","type":"diamond","x":16.75,"y":-129.4609375,"width":221.5,"height":232,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1333690050,"version":65,"versionNonce":1053495966,"isDeleted":true,"boundElements":null,"updated":1727963297824,"link":null,"locked":false},{"id":"syh6TsqfxRecbjpwk3-31","type":"line","x":18.75,"y":-11.4609375,"width":216,"height":1.5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":666316638,"version":65,"versionNonce":890990146,"isDeleted":true,"boundElements":null,"updated":1727963297824,"link":null,"locked":false,"points":[[0,0],[216,1.5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"Hk3XS-jJq1GreXf_ONsLw","type":"line","x":230.25,"y":-8.4609375,"width":152,"height":1.5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":2047776862,"version":133,"versionNonce":1330319070,"isDeleted":true,"boundElements":null,"updated":1727963297824,"link":null,"locked":false,"points":[[0,0],[152,-1.5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"solid","currentItemStrokeWidth":2,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":465.75,"scrollY":337.0390625,"zoom":{"value":1},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Dugga_2024_uppgift_3_24-10-03excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
## 4.

> Fem punkter finns utplacerade inuti en kvadrat med sidlängd 2. Visa att det alltid går att välja två av dessa punkter så att avståndet mellan dem inte överstrider $\sqrt{ 2 }$.

### Lösning

Dela in kvadraten i fyra kvadrater.

Lådprinciper medför att det finns minst en "del" med minst 2 punkter

Längsta avståndet mellan två punkter i en del är diagonalen, med längden $\sqrt{ 2 }$.

<div id="Dugga_2024_uppgift_4_24-10-03excalidraw.md2"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.1.4","elements":[{"type":"rectangle","version":70,"versionNonce":1049288258,"isDeleted":false,"id":"OpCbnHPqMNT_IXUCkbssd","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-200.5,"y":-157.4609375,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":310.5,"height":310.5,"seed":1078293086,"groupIds":[],"frameId":null,"roundness":{"type":3},"boundElements":[{"id":"as-_u6dtj0rdFnoI_Qxw0","type":"arrow"},{"id":"CFF01Z0K-qevUIZzFrFrK","type":"arrow"}],"updated":1727964518777,"link":null,"locked":false},{"type":"line","version":75,"versionNonce":995963102,"isDeleted":false,"id":"Qv32-xAOqJD6ri-jhqkQA","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-53,"y":-157.4609375,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":1.4210854715202004e-14,"height":310,"seed":1264507522,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[-1.4210854715202004e-14,310]]},{"type":"line","version":54,"versionNonce":418468866,"isDeleted":false,"id":"c607skbbNVeutbJkJajTu","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-202,"y":-7.9609375,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":311,"height":0,"seed":938405890,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[311,0]]},{"type":"text","version":49,"versionNonce":762020802,"isDeleted":false,"id":"dHHjXsJr","fillStyle":"solid","strokeWidth":2,"strokeStyle":"dotted","roughness":1,"opacity":100,"angle":0,"x":-54.5,"y":-218.4609375,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":14.239990234375,"height":25,"seed":1763948190,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1727963810706,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"2","rawText":"2","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"2","lineHeight":1.25},{"type":"arrow","version":63,"versionNonce":1406210398,"isDeleted":false,"id":"as-_u6dtj0rdFnoI_Qxw0","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-203,"y":-182.4609375,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":310,"height":0,"seed":2047573378,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false,"startBinding":{"focus":-1.1610305958132046,"gap":25,"elementId":"OpCbnHPqMNT_IXUCkbssd"},"endBinding":null,"lastCommittedPoint":null,"startArrowhead":"arrow","endArrowhead":"arrow","points":[[0,0],[310,0]]},{"type":"arrow","version":150,"versionNonce":1518975874,"isDeleted":false,"id":"CFF01Z0K-qevUIZzFrFrK","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-227,"y":-145.4609375,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":0,"height":132.5,"seed":1987522334,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false,"startBinding":{"elementId":"OpCbnHPqMNT_IXUCkbssd","focus":1.1706924315619969,"gap":26.5},"endBinding":null,"lastCommittedPoint":null,"startArrowhead":"arrow","endArrowhead":"arrow","points":[[0,0],[0,132.5]]},{"type":"text","version":27,"versionNonce":950220190,"isDeleted":false,"id":"hZy7Sgi5","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-257,"y":-91.4609375,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":5.4199981689453125,"height":25,"seed":608459550,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1727963810706,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"1","rawText":"1","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"1","lineHeight":1.25},{"type":"ellipse","version":44,"versionNonce":2123037506,"isDeleted":false,"id":"Hz3zcoWGtO1vjP2hiDCD9","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-147,"y":-103.4609375,"strokeColor":"#1e1e1e","backgroundColor":"#1e1e1e","width":11,"height":11,"seed":1769838942,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false},{"type":"ellipse","version":69,"versionNonce":1076285918,"isDeleted":false,"id":"lpoDVa5cb7BTc16K0s-33","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-0.5,"y":-104.4609375,"strokeColor":"#1e1e1e","backgroundColor":"#1e1e1e","width":11,"height":11,"seed":407004354,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false},{"type":"ellipse","version":103,"versionNonce":1473135362,"isDeleted":false,"id":"gvZ0sGxq7hA4kdxxDCp2n","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-121.5,"y":23.5390625,"strokeColor":"#1e1e1e","backgroundColor":"#1e1e1e","width":11,"height":11,"seed":1276619102,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false},{"type":"ellipse","version":161,"versionNonce":91022878,"isDeleted":false,"id":"jwdmvTX-HgHomh_CPOUe0","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-88.5,"y":100.0390625,"strokeColor":"#1e1e1e","backgroundColor":"#1e1e1e","width":11,"height":11,"seed":1180033346,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false},{"type":"ellipse","version":197,"versionNonce":426144350,"isDeleted":false,"id":"LulpNrE_lRF4d88Kwqt_S","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":0.5,"y":46.5390625,"strokeColor":"#1e1e1e","backgroundColor":"#1e1e1e","width":11,"height":11,"seed":1643679298,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727963810706,"link":null,"locked":false},{"type":"arrow","version":178,"versionNonce":563320094,"isDeleted":false,"id":"7ql_usnIi36DebNjukDQo","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"dashed","roughness":1,"opacity":100,"angle":0,"x":-191.08823529411762,"y":142.77435661764702,"strokeColor":"#1e1e1e","backgroundColor":"#1e1e1e","width":135.58823529411762,"height":148.73529411764702,"seed":1226103234,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1727964521335,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":"arrow","endArrowhead":"arrow","points":[[0,0],[135.58823529411762,-148.73529411764702]]},{"type":"image","version":80,"versionNonce":725113054,"isDeleted":false,"id":"1BUBiHRr","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-150.18915031218484,"y":43.812040441176435,"strokeColor":"#000000","backgroundColor":"transparent","width":22,"height":17,"seed":32152,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1727964515482,"link":null,"locked":false,"status":"pending","fileId":"f7e0d5f8f87dc104267b938358c0f58b819eb0b3","scale":[1,1]},{"type":"text","version":58,"versionNonce":1148387330,"isDeleted":true,"id":"zp8QtSlD","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"dashed","roughness":1,"opacity":100,"angle":0,"x":-130.36562090042014,"y":74.3708639705882,"strokeColor":"#1e1e1e","backgroundColor":"#1e1e1e","width":119.41993713378906,"height":25,"seed":986189826,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1727964512555,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"$\\sqrt{2}$","rawText":"$\\sqrt{2}$","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"$\\sqrt{2}$","lineHeight":1.25}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"#1e1e1e","currentItemFillStyle":"hachure","currentItemStrokeWidth":0.5,"currentItemStrokeStyle":"dashed","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":"arrow","currentItemEndArrowhead":"arrow","scrollX":436.2479738415966,"scrollY":230.9692095588235,"zoom":{"value":1.7000000000000002},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Dugga_2024_uppgift_4_24-10-03excalidraw.md2");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
## 5.

> För två mängder $S_{1}$ och $S_{2}$, antag att $R_{1}$ är en partiell ordning på $S_{1}$ och $R_{2}$ en partiell ordning på $S_{2}$. Definiera en ny relation $R$ på $S_{1}\times S_{2}$ enligt att $(a_{1},a_{2})R(b_{1},b_{2})$ om och endast om något av följande gäller:
> 
>   i) $a_{1}\neq b_{1}$ och $a_{1}R_{1}b_{1}$, eller
>   ii) $a_{1}=b_{1}$ och $a_{2}R_{2}b_{2}$.
> 
> Visa att $R$ är en partiell ordning på $S_{1}\times S_{2}$.
### Lösning

Om $R$ är reflexiv, antisymmetrisk och transitiv är den en partiell ordning på $S_{1}\times S_{2}$.

#### Reflexiv

Tag $(a_{1},a_{2})\in S_{1}\times S_{2}$. Vill visa $(a_{1},a_{2})R(a_{1},a_{2})$

Eftersom $R_{1}$ och $R_{2}$ både är reflexiva, gäller $a_{1}R_{1}a_{1}$ och $a_{2}R_{2}a_{2}$.

$a_{1}=a_{1}\land a_{2}R_{2}a_{2}$ är alltid sant.

#### Antisymmetrisk

Tag $(a_{1},a_{2}),(b_{1},b_{2})\in S_{1}\times S_{2}$
Vill visa $(a_{1},a_{2})R(b_{1},b_{2})\land(b_{1},b_{2})R(a_{1},a_{2})\implies(a_{1},a_{2})=(b_{1},b_{2})$

Antag att $(a_{1},a_{2})R(b_{1},b_{2})\land(b_{1},b_{2})R(a_{1},a_{2})$

Antag också att $a_{1}\neq b_{1}$. Från definitionen av $R$ har vi då:

  $(a_{1},a_{2})R(b_{1},b_{2})\implies a_{1}R_{1}b_{1}$
  $(b_{1},b_{2})R(a_{1},a_{2})\implies b_{1}R_{1}a_{1}$

$R_{1}$ är antisymmetrisk vilket medför att $a_{1}=b_{1}$. **Motsägelse**

$a_{1}=b_{1}$ måste vara sant

Från definitionen av $R$ fås då:

  $(a_{1},a_{2})R(b_{1},b_{2})\implies a_{2}R_{2}b_{2}$
  $(b_{1},b_{2})R(a_{1},a_{2})\implies b_{2}R_{2}a_{2}$

$R_{2}$ är antisymmetrisk vilket medför att $a_{2}=b_{2}$

$(a_{1},a_{2})R(b_{1},b_{2})\land(b_{1},b_{2})R(a_{1},a_{2})\implies a_{1}=b_{1},\enspace a_{2}=b_{2}\iff(a_{1},a_{2})=(b_{1},b_{2})$

D.v.s. $R$ är antisymmetrisk VSV.

#### Transitiv

Tag $(a_{1},a_{2}),(b_{1},b_{2}),(c_{1},c_{2})\in S_{1}\times S_{2}$

Vill visa att $(a_{1},a_{2})R(b_{1},b_{2})\land(b_{1},b_{2})R(c_{1},c_{2})\implies(a_{1},a_{2})R(c_{1},c_{2})$

Antag $(a_{1},a_{2})R(b_{1},b_{2})\land(b_{1},b_{2})R(c_{1},c_{2})$, från det fås att $a_{1}R_{1}b_{1}\land b_{1}R_{1}c_{1}$

$R_{1}$ transitiv$\implies a_{1}R_{1}c_{1}$

Om $a_{1}\neq c_{1}$ ger $a_{1}R_{1}c_{1}$ direkt att $(a_{1},a_{2})R(c_{1},c_{2})$ p.g.a. *i)*.

Antag att $a_{1}=c_{1}$

Från antisymmetri hos $R_{1}$ fås att $a_{1}=b_{1}$ (vi har $a_{1}R_{1}b_{1}$ och $b_{1}R_{1}c_{1}$, $a_{1}=c_{1}$)

$(a_{1}=b_{1}=c_{1})$. Från definitionen av $R$ fås då $a_{2}R_{2}b_{2}$ Dvs, $(b_{1},b_{2})R(c_{1},c_{2})\land b_{1}=c_{1}$
$\enspace\implies b_{2}R_{2}c_{2}$ från *ii)*.

$R_{2}$ transitiv medför att $a_{2}R_{2}c_{2}$
Det medför att $R$ är transitiv VSV.

$R$ reflexiv, antisymmetrisk och transitiv vilket innebär att den är en partiell ordning på $S_{1}\times S_{2}$.
