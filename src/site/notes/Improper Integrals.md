---
{"dg-publish":true,"permalink":"/improper-integrals/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[The Integral|The Integral]], [[Diverging Improper Integrals|Diverging Improper Integrals]]

<style>
.container {font-family: sans-serif; text-align: center;}
.button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;}
.excalidraw .App-menu_top .buttonList { display: flex;}
.excalidraw-wrapper { height: 800px; margin: 50px; position: relative;}
:root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;}
</style><script src="https://unpkg.com/react@17/umd/react.production.min.js"></script><script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://unpkg.com/@excalidraw/excalidraw@0.12.0/dist/excalidraw.production.min.js"></script><div id="Improper_Intergrals_2022-10-31_1003.31.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://excalidraw.com","elements":[{"id":"Cesz2udg-ylEssxH4UY2B","type":"arrow","x":-68,"y":110.55626678466797,"width":2.842170943040401e-14,"height":356.80003356933594,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"round","seed":1576524397,"version":79,"versionNonce":966710029,"isDeleted":false,"boundElements":null,"updated":1667235815766,"link":null,"locked":false,"points":[[0,0],[2.842170943040401e-14,-356.80003356933594]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow"},{"id":"qKGTA4YxqIU874RnH33P_","type":"arrow","x":-220,"y":21.756248474121094,"width":427.20001220703125,"height":0,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"round","seed":1387622467,"version":48,"versionNonce":969735181,"isDeleted":false,"boundElements":null,"updated":1667235819151,"link":null,"locked":false,"points":[[0,0],[427.20001220703125,0]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow"},{"id":"KtTa2Fy3Mmqp_0_oJZO7O","type":"line","x":-277.6000061035156,"y":4.156242370605469,"width":361.6000061035156,"height":178.39999389648438,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"round","seed":1385846595,"version":183,"versionNonce":1821706531,"isDeleted":false,"boundElements":null,"updated":1667235826004,"link":null,"locked":false,"points":[[0,0],[166.39999389648438,-37.600006103515625],[361.6000061035156,-178.39999389648438]],"lastCommittedPoint":[361.6000061035156,-178.39999389648438],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"JIprdyCMYjDE-3G55LlO-","type":"line","x":-268.79998779296875,"y":16.935749993669816,"width":200.00000003206654,"height":74.37951372657994,"angle":0,"strokeColor":"#000000","backgroundColor":"#4c6ef5","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"sharp","seed":66972867,"version":374,"versionNonce":1141186019,"isDeleted":false,"boundElements":null,"updated":1667235862998,"link":null,"locked":false,"points":[[0,0],[2.3999938968691463,-14.142930227440667],[125.59997560607526,-33.543939619410295],[197.59997561761918,-74.37951372657993],[200.00000003206654,0],[0,0]],"lastCommittedPoint":[-3.20001220703125,1.600006103515625],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#000000","currentItemBackgroundColor":"#4c6ef5","currentItemFillStyle":"hachure","currentItemStrokeWidth":0.5,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStrokeSharpness":"sharp","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemLinearStrokeSharpness":"sharp","gridSize":null,"colorPalette":{}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Improper_Intergrals_2022-10-31_1003.31.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

$$
\int_{a}^{b} f(x)dx
$$
Where $a$ and/or $b$ is:
- A value not in the domain of $f$
- or $\pm\infty$

---
To solve these, we use [[The Limit|The Limit]]:

$$
\int_{-\infty}^{0} e^{x}dx = \lim_{a\rightarrow -\infty} \int_{a}^{0} e^{x} dx
$$


$$
\begin{align}
&= \lim_{a\rightarrow -\infty} e ^{x} \bigg|_{a}^{0} \\
&= \lim_{a\rightarrow  -\infty}(e^{0} - e^{a}) \\
&= \lim_{a\rightarrow -\infty}(1-e^{a}) \\
&= 1 - e^{-\infty} \\
&= \boxed1 \textcolor{orange}{\leftarrow\text{converges}}
\end{align}
$$

Keep in mind [[Diverging Improper Integrals|Diverging Improper Integrals]]