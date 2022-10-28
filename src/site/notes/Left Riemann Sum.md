---
{"dg-publish":true,"permalink":"/left-riemann-sum/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
> [[MAT 150 Hub|MAT 150 Hub]], [[Riemann Sums|Riemann Sums]]

<style>
.container {font-family: sans-serif; text-align: center;}
.button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;}
.excalidraw .App-menu_top .buttonList { display: flex;}
.excalidraw-wrapper { height: 800px; margin: 50px; position: relative;}
:root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;}
</style><script src="https://unpkg.com/react@17/umd/react.production.min.js"></script><script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://unpkg.com/@excalidraw/excalidraw@0.12.0/dist/excalidraw.production.min.js"></script><div id="Reimann_Sums_2022-10-17_1056.58.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://excalidraw.com","elements":[{"type":"rectangle","version":315,"versionNonce":1111670259,"isDeleted":false,"id":"SYv4K0itcVo0iXGGULOR5","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-50.00046052621572,"y":-115.33187291621763,"strokeColor":"#c92a2a","backgroundColor":"#fa5252","width":66.95272459336533,"height":47.41032014560478,"seed":1212891037,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666029648126,"link":null,"locked":false},{"type":"line","version":742,"versionNonce":113675965,"isDeleted":false,"id":"3OG2fbQry42Rf7V_6fdvn","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-66.38630384329426,"y":-106.66656684139997,"strokeColor":"#000000","backgroundColor":"#fa5252","width":244.24290799633707,"height":76.867860967502,"seed":1734034429,"groupIds":[],"strokeSharpness":"round","boundElements":[],"updated":1666029648126,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[72.48271518725107,-32.28621715641822],[244.24290799633707,-76.867860967502]]},{"type":"rectangle","version":530,"versionNonce":431785875,"isDeleted":false,"id":"LCQVPU6NKNdM_Qpgsox8U","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":20.178929387997115,"y":-144.34789297563407,"strokeColor":"#c92a2a","backgroundColor":"#fa5252","width":66.95272459336533,"height":76.19936098589324,"seed":1118551133,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666029648126,"link":null,"locked":false},{"type":"rectangle","version":652,"versionNonce":375059805,"isDeleted":false,"id":"peeVFP6b6ov4oe7ERvR0D","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":90.99327200617583,"y":-162.884467419858,"strokeColor":"#c92a2a","backgroundColor":"#fa5252","width":66.95272459336533,"height":94.30738354435084,"seed":1645095101,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666029654032,"link":null,"locked":false}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#000000","currentItemBackgroundColor":"#fa5252","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":0,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStrokeSharpness":"sharp","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemLinearStrokeSharpness":"round","gridSize":null,"colorPalette":{}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Reimann_Sums_2022-10-17_1056.58.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

$$
\begin{align}
&\sum\limits_{i=0}^{N-1} f(a+i\Delta x) \Delta x \\
&\text{Let } N = \frac{b-a}{\Delta x} \textcolor{gray}{\text{ number of steps }}
\end{align}
$$

### Too High
When **slope of $y'$ is $\lt 0$**

### Too Low
When **slope of $y'$ is $\gt 0$**