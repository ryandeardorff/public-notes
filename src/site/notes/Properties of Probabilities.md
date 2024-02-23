---
{"dg-publish":true,"permalink":"/properties-of-probabilities/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

1. $P(\emptyset)=0$
2. $P(E^{C}) = 1-P(E)$
3. If $E$ and $F$ are events, then $P(E\cup F) = P(E)+P(F)-P(E\cap F)$

Proofs:
1.
$$
\begin{align*}
\Omega &= \Omega \cup \emptyset\\
\Omega&\cap\emptyset = \emptyset
\end{align*}$$
By [[Axioms of Probability#^ebd440|axiom 3]]:
$$
\begin{align*}
P(\Omega\cup\emptyset) &= P(\Omega) + P(\emptyset)\\
P(\Omega) &= P(\Omega)+P(\emptyset)\\
P(\emptyset) &= 0
\end{align*}
$$

2.
$$
E\cup E^{C} = \Omega
$$
$$
E\cap E^{C}= \emptyset
$$
By [[Axioms of Probability#^ebd440|axiom 3]]:
$$
\begin{align*}
P(\Omega) &= P(E\cup E^{C}) = P(E)+P(E^{C})
\end{align*}
$$
By [[Axioms of Probability#^06b86d| axiom 1]]:
$$
\begin{align*}
1&= P(E) + P(E^{C})\\
P(E^{C})&=  1-P(E)
\end{align*}
$$

3.
<style>
.container {font-family: sans-serif; text-align: center;}
.button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;}
.excalidraw .App-menu_top .buttonList { display: flex;}
.excalidraw-wrapper { height: 800px; margin: 50px; position: relative;}
:root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;}
</style><script src="https://unpkg.com/react@17/umd/react.production.min.js"></script><script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://unpkg.com/@excalidraw/excalidraw@0.12.0/dist/excalidraw.production.min.js"></script><div id="Properties_of_Probabilities_2024-02-09_0933.45.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.9.19","elements":[{"id":"zevknNVhBrX63eIwf-uxZ","type":"rectangle","x":-226,"y":-267.75,"width":339,"height":339,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":3},"seed":942823432,"version":62,"versionNonce":121084680,"isDeleted":false,"boundElements":null,"updated":1707500030820,"link":null,"locked":false},{"id":"OzNOTEPH-bDBteIRQy-Kz","type":"ellipse","x":-166,"y":-199.75,"width":130,"height":130,"angle":0,"strokeColor":"#1971c2","backgroundColor":"#a5d8ff","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":721659000,"version":52,"versionNonce":869334792,"isDeleted":false,"boundElements":null,"updated":1707500050358,"link":null,"locked":false},{"id":"Onoa1hLK","type":"text","x":-164,"y":-218.75,"width":13.479995727539062,"height":25,"angle":0,"strokeColor":"#1971c2","backgroundColor":"#a5d8ff","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":1829262712,"version":4,"versionNonce":107732488,"isDeleted":false,"boundElements":null,"updated":1707500050358,"link":null,"locked":false,"text":"E","rawText":"E","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":18,"containerId":null,"originalText":"E","lineHeight":1.25},{"id":"SRj_Oo3Rr1Y3G24PjA1hj","type":"ellipse","x":-87,"y":-147.75,"width":130,"height":130,"angle":0,"strokeColor":"#e03131","backgroundColor":"#ffc9c9","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1203927304,"version":99,"versionNonce":1022167672,"isDeleted":false,"boundElements":null,"updated":1707500065907,"link":null,"locked":false},{"id":"daHSPHLZ","type":"text","x":54,"y":-127.75,"width":11.479995727539062,"height":25,"angle":0,"strokeColor":"#e03131","backgroundColor":"#ffc9c9","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":831292680,"version":124,"versionNonce":471398664,"isDeleted":false,"boundElements":null,"updated":1707500065907,"link":null,"locked":false,"text":"F","rawText":"F","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":18,"containerId":null,"originalText":"F","lineHeight":1.25},{"type":"image","version":180,"versionNonce":1246650376,"isDeleted":false,"id":"xs76D4fl","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":128.5,"y":-236,"strokeColor":"#000000","backgroundColor":"transparent","width":45,"height":26.052631578947366,"seed":24778,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1707500089862,"link":null,"locked":false,"status":"pending","fileId":"d7ecdf7f964fcbcde9dd07bf6f88da23e95944da","scale":[1,1]}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#e03131","currentItemBackgroundColor":"#ffc9c9","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":397,"scrollY":412.25,"zoom":{"value":1},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Properties_of_Probabilities_2024-02-09_0933.45.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
$P(E\cup F) = P(E) + P(\textcolor{red}{red})$ by [[Axioms of Probability#^ebd440|axiom 3]]
$P(\textcolor{red}{red}) = P(F) - P(E\cap F)$ b/c
$(red)\cup (E\cap F) = F$ and $red \cap (E\cap F)$ = $\emptyset$
By [[Axioms of Probability#^ebd440|axiom 3]]: $P(F) = P(red) + P(E\cap F)$
Get $P(E\cup F) = P(E) + P(F) - P(E\cap F)$