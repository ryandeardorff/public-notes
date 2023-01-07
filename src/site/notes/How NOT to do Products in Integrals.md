---
{"dg-publish":true,"permalink":"/how-not-to-do-products-in-integrals/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
>[[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[Products in Integrals|Products in Integrals]]

**DO NOT DO THIS!!!!**
$$
\int (x+1)(x+4) \ dx \textcolor{red}{\ne \int (x+1) dx \int (x+4)dx}
$$

But why? 😦

Remember [[Summations|Summations]]:
$$
\begin{align}
&[(1+1)(1+4) + (1.1 + 1)(1.1 + 4) + \dots] \times 0.1 \\
&[2\times 5 + 2.1 \times 5.1 + \dots] \times 0.1
\end{align}
$$
We can't bring out those out!
That would be like trying to do the area of the rectangles by adding their side lengths and finding that area:
<style>
.container {font-family: sans-serif; text-align: center;}
.button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;}
.excalidraw .App-menu_top .buttonList { display: flex;}
.excalidraw-wrapper { height: 800px; margin: 50px; position: relative;}
:root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;}
</style><script src="https://unpkg.com/react@17/umd/react.production.min.js"></script><script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://unpkg.com/@excalidraw/excalidraw@0.12.0/dist/excalidraw.production.min.js"></script><div id="Quotients_in_Integrals_2022-10-24_1031.16.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://excalidraw.com","elements":[{"type":"rectangle","version":138,"versionNonce":1474418677,"isDeleted":false,"id":"2WYUu2gB7SGir4VevR37D","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-312,"y":66.55623626708986,"strokeColor":"#000000","backgroundColor":"transparent","width":116,"height":120.80001831054686,"seed":766078453,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666632705528,"link":null,"locked":false},{"type":"rectangle","version":131,"versionNonce":326241461,"isDeleted":false,"id":"x6BnIlpK8GqzzXMdpYSqj","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-192.4000244140625,"y":-44.84375762939453,"strokeColor":"#000000","backgroundColor":"transparent","width":116,"height":231.20001220703125,"seed":212737365,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666632684832,"link":null,"locked":false},{"type":"rectangle","version":398,"versionNonce":192608219,"isDeleted":false,"id":"ULEWM-EvOV3BzZojUE0P8","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-71,"y":-169.24381256103516,"strokeColor":"#000000","backgroundColor":"transparent","width":116,"height":352.0000305175781,"seed":307573685,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666632707379,"link":null,"locked":false},{"type":"rectangle","version":184,"versionNonce":255554523,"isDeleted":false,"id":"TRw0Z7bfXMGTyBh1iB8v2","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-316.79998779296875,"y":-538.0937576293946,"strokeColor":"#0b7285","backgroundColor":"transparent","width":362.39996337890625,"height":724.0000000000001,"seed":1051018363,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1666632795287,"link":null,"locked":false}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#0b7285","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStrokeSharpness":"sharp","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemLinearStrokeSharpness":"round","gridSize":null,"colorPalette":{}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Quotients_in_Integrals_2022-10-24_1031.16.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>