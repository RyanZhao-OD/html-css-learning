## 解析和渲染


> 解析是指浏览器生成 DOM 树结构（此时用户不一定能看到，但脚本比如 querySelectorAll 可以访问到）；渲染是指浏览器把 DOM 树与 CSS 结合进行布局并绘制到屏幕（此时用户是可以看到的）。

- CSS（外链或内联）会阻塞整个DOM的渲染（Rendering），然而DOM解析（Parsing）会正常进行
- 很多浏览器中，CSS会延迟脚本执行和DOMContentLoaded事件
- JS（外链或内联）会阻塞后续DOM的解析（Parsing），延迟 DOMContentLoaded，后续DOM的渲染（Rendering）也将被阻塞
- JS前的DOM可以正常解析（Parsing）和渲染（Rendering）