---
{"dg-publish":true,"permalink":"/sum-rule-for-integrals/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[Properties of Integrals|Properties of Integrals]]

$$
\int f(x)+g(x) \ dx = \int f(x)dx + \int g(x)dx
$$

^bd7249

<style>
.container {font-family: sans-serif; text-align: center;}
.button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;}
.excalidraw .App-menu_top .buttonList { display: flex;}
.excalidraw-wrapper { height: 800px; margin: 50px; position: relative;}
:root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;}
</style><script src="https://unpkg.com/react@17/umd/react.production.min.js"></script><script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://unpkg.com/@excalidraw/excalidraw@0.12.0/dist/excalidraw.production.min.js"></script><div id="Sum_Rule_for_Integrals_2022-10-24_1014.45.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://excalidraw.com","elements":[{"id":"oc33QclEw8IiCm1HcIqt2","type":"arrow","x":-212,"y":164.15621185302734,"width":494.4000244140625,"height":0,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"round","seed":661377717,"version":91,"versionNonce":2003892027,"isDeleted":false,"boundElements":null,"updated":1666631696566,"link":null,"locked":false,"points":[[0,0],[494.4000244140625,0]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow"}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#000000","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStrokeSharpness":"sharp","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemLinearStrokeSharpness":"round","gridSize":null,"colorPalette":{}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Sum_Rule_for_Integrals_2022-10-24_1014.45.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

---
### Why?
Remember, it's a [[Summations|summation]]...
$$
\begin{align}
&(f(1)+g(1)) + (f(1.1)+g(1.1)) + \dots) \times 0.1 \\
=&(f(1)+f(1.1)+ \dots + g(1) + g(1.1)+ \dots) \times 0.1
\end{align}
$$
Or remember [[Intro to the Antiderivative|Antiderivatives]]
$$
\begin{align}
&F(x)+C + G(x) + C = F(x)+G(x) + C\\ \\
& \frac{d}{dx}(F(x)+G(x)+C) = F'(x)+ G'(x) = f(x)+g(x) \\
\end{align}
$$
*The $C$ is a placeholder.*