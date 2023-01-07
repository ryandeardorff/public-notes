---
{"dg-publish":true,"permalink":"/right-riemann-sum/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[Riemann Sums|Riemann Sums]]

<style>
.container {font-family: sans-serif; text-align: center;}
.button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;}
.excalidraw .App-menu_top .buttonList { display: flex;}
.excalidraw-wrapper { height: 800px; margin: 50px; position: relative;}
:root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;}
</style><script src="https://unpkg.com/react@17/umd/react.production.min.js"></script><script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://unpkg.com/@excalidraw/excalidraw@0.12.0/dist/excalidraw.production.min.js"></script><div id="Reimann_Sums_2022-10-17_1059.00.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://excalidraw.com","elements":[{"type":"rectangle","version":346,"versionNonce":59701235,"isDeleted":false,"id":"8ClB340OEPfi8uYjPlf_b","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-168.73561068108998,"y":-68.84763415233914,"strokeColor":"#c92a2a","backgroundColor":"#fa5252","width":66.95272459336533,"height":70.6103018350579,"seed":1798965341,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666029664266,"link":null,"locked":false},{"type":"line","version":773,"versionNonce":45034205,"isDeleted":false,"id":"dKnI83vwAmMlHObxa_9oE","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-185.12145399816853,"y":-36.98234638806832,"strokeColor":"#000000","backgroundColor":"#fa5252","width":241.44292020336832,"height":77.26785486398637,"seed":2062742717,"groupIds":[],"strokeSharpness":"round","boundElements":[],"updated":1666029680398,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[78.88270908373545,-31.486214104660405],[159.8876528649337,-58.64572946592554],[241.44292020336832,-77.26785486398637]]},{"type":"rectangle","version":551,"versionNonce":294770483,"isDeleted":false,"id":"vZbKK2eYM6ss4QIE6F2vu","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-98.55622076687715,"y":-93.0636664187868,"strokeColor":"#c92a2a","backgroundColor":"#fa5252","width":66.95272459336533,"height":94.59935488237761,"seed":294606109,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666029664266,"link":null,"locked":false},{"type":"rectangle","version":668,"versionNonce":2052487379,"isDeleted":false,"id":"Uu9cyCmdXIrlfvyG-m3sN","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-28.541865941667197,"y":-110.800253070042,"strokeColor":"#c92a2a","backgroundColor":"#fa5252","width":66.95272459336533,"height":111.90738964786647,"seed":1786816893,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666029664266,"link":null,"locked":false}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#000000","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":0,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStrokeSharpness":"sharp","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemLinearStrokeSharpness":"round","gridSize":null,"colorPalette":{}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Reimann_Sums_2022-10-17_1059.00.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

$$
\begin{align}
&\sum\limits_{i=1}^{N} f(a+i\Delta x) \Delta x \\
&\text{Let } N = \frac{b-a}{\Delta x} \textcolor{gray}{\text{ number of steps }}
\end{align}
$$

### Too High
When **slope of $y'$ is $\gt 0$**

### Too Low
When **slope of $y'$ is $\lt 0$**