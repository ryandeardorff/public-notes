---
{"dg-publish":true,"permalink":"/trigonometric-substitution-trig-functions-appearing-in-non-trig-integrals/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]]

<style>
.container {font-family: sans-serif; text-align: center;}
.button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;}
.excalidraw .App-menu_top .buttonList { display: flex;}
.excalidraw-wrapper { height: 800px; margin: 50px; position: relative;}
:root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;}
</style><script src="https://unpkg.com/react@17/umd/react.production.min.js"></script><script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://unpkg.com/@excalidraw/excalidraw@0.12.0/dist/excalidraw.production.min.js"></script><div id="UNDF_2023-01-17_1313.23.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://excalidraw.com","elements":[{"id":"wzIeo5nHNfBTtT8qcH1D2","type":"arrow","x":-67.20001220703125,"y":98.55626678466797,"width":0,"height":262.4000244140625,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"round","seed":1922895102,"version":102,"versionNonce":932180094,"isDeleted":false,"boundElements":null,"updated":1673990103919,"link":null,"locked":false,"points":[[0,0],[0,-262.4000244140625]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow"},{"type":"arrow","version":442,"versionNonce":1040440930,"isDeleted":false,"id":"BJx_1qL9-kfsKYegrt5EZ","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-204.40002441406256,"y":-24.64377593994141,"strokeColor":"#000000","backgroundColor":"transparent","width":279.60003662109375,"height":0,"seed":2090450402,"groupIds":[],"strokeSharpness":"round","boundElements":[],"updated":1673990103920,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":"arrow","points":[[0,0],[279.60003662109375,0]]},{"id":"jly9V2fzQ3CYQENdO66by","type":"line","x":-170.39996337890625,"y":-26.243751525878906,"width":208,"height":76,"angle":0,"strokeColor":"#000000","backgroundColor":"#868e96","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"round","seed":1970576958,"version":297,"versionNonce":1326881086,"isDeleted":false,"boundElements":null,"updated":1673990103920,"link":null,"locked":false,"points":[[0,0],[43.199951171875,-51.20001220703125],[104,-73.60000610351562],[173.5999755859375,-52],[208,2.399993896484375]],"lastCommittedPoint":[208,2.399993896484375],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"dr4MvqhnbMBxw83tVwglZ","type":"line","x":-27.20001220703125,"y":-91.6437759399414,"width":0,"height":65.60000610351562,"angle":0,"strokeColor":"#000000","backgroundColor":"#868e96","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"sharp","seed":1705820542,"version":66,"versionNonce":1190172002,"isDeleted":false,"boundElements":null,"updated":1673990112325,"link":null,"locked":false,"points":[[0,0],[0,65.60000610351562]],"lastCommittedPoint":[0,65.60000610351562],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"IjQRhavm","type":"image","x":-35.5,"y":-133.0875015258789,"width":101,"height":24,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"strokeSharpness":"sharp","seed":73425,"version":43,"versionNonce":57063486,"updated":1673990130685,"isDeleted":false,"groupIds":[],"boundElements":[],"link":null,"locked":false,"fileId":"d6308fb4da79baa30768deea657d7674af29801e","scale":[1,1]},{"id":"0Kfari1Q","type":"text","x":-41,"y":-19.24378204345703,"width":31,"height":25,"angle":0,"strokeColor":"#000000","backgroundColor":"#868e96","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"strokeSharpness":"sharp","seed":401096894,"version":50,"versionNonce":2003212258,"isDeleted":false,"boundElements":null,"updated":1673990141502,"link":null,"locked":false,"text":"1/2","rawText":"1/2","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":18,"containerId":null,"originalText":"1/2"},{"id":"z0VZqJ0DYwvIdP11IylAO","type":"rectangle","x":-68,"y":-98.8437271118164,"width":41.60003662109375,"height":79.199951171875,"angle":0,"strokeColor":"#000000","backgroundColor":"#868e96","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":30,"groupIds":[],"strokeSharpness":"sharp","seed":944589730,"version":91,"versionNonce":615721726,"isDeleted":false,"boundElements":null,"updated":1673990157833,"link":null,"locked":false}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#000000","currentItemBackgroundColor":"#868e96","currentItemFillStyle":"hachure","currentItemStrokeWidth":0.5,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":30,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStrokeSharpness":"sharp","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemLinearStrokeSharpness":"sharp","gridSize":null,"colorPalette":{}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("UNDF_2023-01-17_1313.23.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
Get the area under the semicircle.

$$
\begin{align}
& \int_{0}^{\frac{1}{2}} \sqrt{1-x^{2}} \,  dx \\
\end{align}
$$
$u$ sub is going to only get us so far here.

We are going to do:
$$
\begin{align}
x=\sin\theta \\
dx = \cos\theta \, d \theta\\
\end{align}
$$

This gets us:
$$
\begin{align}
&\int \sqrt{1-\sin^{2}\theta} \cos\theta \, d\theta \\
&= \int \cos\theta\cos\theta \, d\theta \\
&= \int \cos^{2}\theta \, d\theta \\
&= \int \frac{1}{2}+ \frac{1}{2}\cos2\theta \, d\theta \\
&= \frac{1}{2}\theta + \frac{1}{4}\sin2\theta + C
\end{align}
$$

Fun... Look at this:
$$
x=\sin\theta \rightarrow \arcsin x = \theta
$$

$$
\begin{align}
&=\frac{1}{2} \arcsin{x} + \frac{1}{4}(2\sin\theta\cos\theta) + C\\
&= \boxed{\frac{1}{2}\arcsin{x} + \frac{1}{2} x \sqrt{1-x^{2}} + C} \\
\end{align}
$$

(this is not quite the end of the problem, but you get the idea, it's just [[Definite integrals and u-substitution|Definite integrals and u-substitution]] from there)