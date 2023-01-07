---
{"dg-publish":true,"permalink":"/kinematics-examples/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#physics 
> [[PHY200 Hub - Motion Dynamics|PHY200 Hub - Motion Dynamics]]

### Example 1: Car up to speed
<style>
.container {font-family: sans-serif; text-align: center;}
.button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;}
.excalidraw .App-menu_top .buttonList { display: flex;}
.excalidraw-wrapper { height: 800px; margin: 50px; position: relative;}
:root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;}
</style><script src="https://unpkg.com/react@17/umd/react.production.min.js"></script><script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://unpkg.com/@excalidraw/excalidraw@0.12.0/dist/excalidraw.production.min.js"></script><div id="Kinematics_Examples_2023-01-06_1858.01.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://excalidraw.com","elements":[{"type":"rectangle","version":211,"versionNonce":420455750,"isDeleted":false,"id":"XiTtv3umB--XLl8Pj2xzl","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-757.276935648457,"y":-102.52787982857285,"strokeColor":"#000000","backgroundColor":"transparent","width":97.60009765625,"height":49.600006103515625,"seed":385381126,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1673060364307,"link":null,"locked":false},{"type":"ellipse","version":170,"versionNonce":2099034650,"isDeleted":false,"id":"qEKGEY30qaYpOPxJBBe4B","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-759.3358355138037,"y":-52.75736323040968,"strokeColor":"#000000","backgroundColor":"transparent","width":20,"height":20,"seed":1723867718,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1673060364307,"link":null,"locked":false},{"type":"ellipse","version":213,"versionNonce":2075593862,"isDeleted":false,"id":"fN-JnEkF6fSoNEl9moq7y","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-678.7195275892664,"y":-52.77053260419359,"strokeColor":"#000000","backgroundColor":"transparent","width":20,"height":20,"seed":407890310,"groupIds":[],"strokeSharpness":"sharp","boundElements":[],"updated":1673060364307,"link":null,"locked":false},{"type":"arrow","version":207,"versionNonce":141715162,"isDeleted":false,"id":"p65igDttK40BM4LMVGcCx","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-711.4115020882391,"y":-78.25108804417096,"strokeColor":"#000000","backgroundColor":"transparent","width":92.14753964320158,"height":0,"seed":1393932122,"groupIds":[],"strokeSharpness":"round","boundElements":[],"updated":1673060364307,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":"arrow","points":[[0,0],[92.14753964320158,0]]},{"type":"line","version":164,"versionNonce":997166022,"isDeleted":false,"id":"bzaDNkkNP3gnIPA8uFKHc","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"angle":0,"x":-795.6151712816533,"y":-32.17733337406935,"strokeColor":"#000000","backgroundColor":"transparent","width":440.0836592889593,"height":0,"seed":1071595206,"groupIds":[],"strokeSharpness":"round","boundElements":[],"updated":1673060364307,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[440.0836592889593,0]]},{"id":"g0OzevsK","type":"image","x":-728.0731429725421,"y":-138.80057355989806,"width":50,"height":18,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"strokeSharpness":"sharp","seed":33311,"version":1,"versionNonce":380818253,"updated":1673060355316,"isDeleted":false,"groupIds":[],"boundElements":[],"link":null,"locked":false,"fileId":"fefcbcc2f263b050fde5d2ba6600aaee4c3f8f86","scale":[1,1]}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#000000","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":0,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStrokeSharpness":"sharp","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemLinearStrokeSharpness":"round","gridSize":null,"colorPalette":{}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Kinematics_Examples_2023-01-06_1858.01.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
$$
\vec{a}_{x}= 10 \, \frac{m}{s^{2}}
$$
We have a car at rest.

We want to find at what time $t$ will it hit $50\, m/s$?

```ad-check
title:Solution
collapse:
$$
\begin{align}
\vec{v}(t) &= \vec{v}_{0} + \vec{a}t \\
\vec{v}(t) &= \left(50 \frac{m}{s}\right) \hat{x}= 10 \frac{m}{s^{2}} \hat{x}\cdot t\\
\frac{50 \, m/s}{10 \, m/s^{2} } &= t\\
t &= \boxed{5 s}
\end{align}
$$
```


