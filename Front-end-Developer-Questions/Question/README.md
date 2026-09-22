# 前端开发面试题 （题目列表页）


## <a name='list'>目录</a>

  1. [前言](#preface)
  1. [HTML部分](#html)
  1. [CSS部分](#css)
  1. [JavaScript部分](#js)
  1. [前端框架](#framework)
  1. [工程化与构建](#eng)

  1. [AI 时代的Web工程实践](#ai)

  1. [其他问题](#other)
  1. [前端学习网站推荐](#web)



## <a name='preface'>前言</a>

 [前言](https://github.com/markyun/My-blog/tree/master/Front-end-Developer-Questions "前言")

## <a name='html'>HTML</a>

- Doctype作用？严格模式与混杂模式如何区分？它们有何意义?

- HTML5 为什么只需要写 <!DOCTYPE HTML>？

- 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？

- 页面导入样式时，使用link和@import有什么区别？

- 介绍一下你对浏览器内核的理解？

- 常见的浏览器内核有哪些？

- html5有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和 HTML5？

- 简述一下你对HTML语义化的理解？

- HTML5的离线储存怎么使用，工作原理能不能解释一下？

- 浏览器是怎么对HTML5的离线储存资源进行管理和加载的呢？

- 请描述一下 cookies，sessionStorage 和 localStorage 的区别？

- iframe有那些缺点？

- Label的作用是什么？是怎么用的？（加 for 或 包裹）

- HTML5的form如何关闭自动完成功能？

- 如何实现浏览器内多个标签页之间的通信? (阿里)

- webSocket如何兼容低浏览器？(阿里)

- 页面可见性（Page Visibility API） 可以有哪些用途？

- 如何在页面上实现一个圆形的可点击区域？

- 实现不使用 border 画出1px高的线，在不同浏览器的Quirksmode和CSSCompat模式下都能保持同一效果。

- 网页验证码是干嘛的，是为了解决什么安全问题？

- title与h1的区别、b与strong的区别、i与em的区别？

- 谈谈你对 Web Components 的理解？自定义元素、Shadow DOM、HTML Template 分别解决什么问题？

- 多标签页之间的状态同步你怎么处理？（storage 事件 / BroadcastChannel / SharedWorker）

- cookie、sessionStorage、localStorage、IndexedDB 各自的大小限制和使用场景？大量结构化数据怎么存？

- Page Lifecycle API（frozen / discarded）了解吗？和页面可见性 API 什么关系？

- 移动端 100vh 为什么会被浏览器地址栏遮挡？现在怎么解决？（字节）

- 无障碍（A11y）做过吗？ARIA 属性了解多少？语义化标签和 tabindex、focus 顺序的关系？

- 首屏体验现在用什么指标度量？（FCP / LCP / INP / CLS）


- iframe 现在还有哪些合理的使用场景？跨 iframe 通信怎么做？sandbox 属性有哪些坑？

- 浏览器的存储方案怎么选？Cookie / localStorage / sessionStorage / IndexedDB / Cache Storage，各自的边界和坑。

- 从输入 URL 到页面完全展示，中间都经历了哪些过程？

- Web Worker 现在能干什么？SharedArrayBuffer + Atomics 解决了什么问题？什么场景值得上 Worker？

- 剪贴板的现代 API 怎么用？和老 execCommand 比好在哪？权限怎么申请？

- 图片懒加载怎么实现？C 端项目里你会关注哪些细节？（米哈游面经）

- 从输入域名到拿到 IP，DNS 的完整查询链路？HTTPS 时代 SNI 还有什么隐私问题？（米哈游面经）

## <a name='css'>CSS</a>

- 介绍一下标准的CSS的盒子模型？低版本IE的盒子模型有什么不同的？

- CSS选择符有哪些？哪些属性可以继承？

- CSS优先级算法如何计算？

- CSS3新增伪类有那些？

- 如何居中div？如何居中一个浮动元素？如何让绝对定位的div居中？

- display有哪些值？说明他们的作用。

- position的值relative和absolute定位原点是？

- CSS3有哪些新特性？

- 请解释一下CSS3的Flexbox（弹性盒布局模型）,以及适用场景？

- 用纯CSS创建一个三角形的原理是什么？

- css多列等高如何实现？

- 一个满屏 品 字布局 如何设计?

- 经常遇到的浏览器的兼容性有哪些？原因，解决方法是什么，常用hack的技巧 ？

- li与li之间有看不见的空白间隔是什么原因引起的？有什么解决办法？

- 为什么要初始化CSS样式?

- absolute的containing block计算方式跟正常流有什么不同？

- CSS里的visibility属性有个collapse属性值是干嘛用的？在不同浏览器下以后什么区别？

- position跟display、margin collapse、overflow、float这些特性相互叠加后会怎么样？

- 对BFC规范(块级格式化上下文：block formatting context)的理解？

- CSS权重优先级是如何计算的？

- 请解释一下为什么需要清除浮动？清除浮动的方式

- zoom:1的清楚浮动原理?

- 移动端的布局用过媒体查询吗？

- 使用 CSS 预处理器吗？喜欢那个？

- CSS优化、提高性能的方法有哪些？

- 浏览器是怎样解析CSS选择器的？

- 在网页中的应该使用奇数还是偶数的字体？为什么呢？

- margin和padding分别适合什么场景使用？

- 抽离样式模块怎么写，说出思路，有无实践经验？[阿里航旅的面试题]

- 元素竖向的百分比设定是相对于容器的高度吗？

- 全屏滚动的原理是什么？用到了CSS的那些属性？

- 什么是响应式设计？响应式设计的基本原理是什么？如何兼容低版本的IE？

- 视差滚动效果，如何给每页做不同的动画？（回到顶部，向下滑动要再次出现，和只出现一次分别怎么做？）

- ::before 和 :after中双冒号和单冒号 有什么区别？解释一下这2个伪元素的作用。

- 如何修改chrome记住密码后自动填充表单的黄色背景 ？

- 你对line-height是如何理解的？

- 设置元素浮动后，该元素的display值是多少？（自动变成display:block）

- 怎么让Chrome支持小于12px 的文字？

- 让页面里的字体变清晰，变细用CSS怎么做？（-webkit-font-smoothing: antialiased;）

- font-style属性可以让它赋值为“oblique” oblique是什么意思？

- position:fixed;在android下无效怎么处理？

- 如果需要手动写动画，你认为最小时间间隔是多久，为什么？（阿里）

- display:inline-block 什么时候会显示间隙？(携程)

- overflow: scroll时不能平滑滚动的问题怎么处理？

- 有一个高度自适应的div，里面有两个div，一个高度100px，希望另一个填满剩下的高度。

- png、jpg、gif 这些图片格式解释一下，分别什么时候用。有没有了解过webp？

- 什么是Cookie 隔离？（或者说：请求资源的时候不要让它带cookie怎么做）

- style标签写在body后与body前有什么区别？

- 什么是CSS 预处理器 / 后处理器？

- rem布局的优缺点

- CSS 原生嵌套（Nesting）和 Less/Sass 的嵌套有什么区别？还需要预处理器吗？

- :has() 选择器为什么被称为"父选择器"？举一个你的实际使用场景？

- 容器查询（Container Queries）和媒体查询的区别？为什么说它更适合组件化开发？

- @layer（层叠层）解决什么问题？和用 !important 硬怼优先级有什么本质区别？

- CSS 自定义属性（CSS 变量）和预处理器变量的区别？运行时主题切换/暗色模式怎么做？

- color-mix()、oklch() 这些现代颜色函数用过吗？

- View Transitions API 了解吗？现在做页面/路由转场动画的标准做法是什么？

- 如何看待 Tailwind 这类原子化 CSS？它的优缺点，你们项目里怎么选型？（阿里）

- browserslist、autoprefixer、PostCSS 现在的定位发生了什么变化？

- 双栏/三栏自适应布局你现在怎么写？（Grid minmax + auto-fit / 容器查询组合拳）

- 深/浅主题切换你怎么架构？next-themes 这类方案的 FOUC 问题怎么解决？

- Tailwind 和原生 CSS 增强（嵌套/:has()/容器查询/@layer）都落地了，2026 年 CSS 该怎么选型？

- 设计系统的前端落地：design token 怎么建模？组件库、主题、文档怎么协作？

- :focus-visible 解决什么问题？自定义控件（div 做的按钮）怎么补全交互语义？

- 响应式的现在时：容器查询、dvh、min()/clamp()、aspect-ratio 组合起来怎么用？

- @property 和 CSS Houdini 给 CSS 带来什么？说一个 @property 的真实用法。

- will-change 的作用是什么？为什么不能给所有动画元素都加上？（QQ音乐面经）

## <a name='js'>JavaScript</a>

-  介绍JavaScript的基本数据类型。

-  说说写JavaScript的基本规范？

-  JavaScript原型，原型链 ? 有什么特点？

-  JavaScript有几种类型的值？（堆：原始数据类型和 栈：引用数据类型），你能画一下他们的内存图吗？

-  Javascript如何实现继承？

-  Javascript创建对象的几种方式？

-  Javascript作用链域?

-  谈谈this对象的理解。

-  eval是做什么的？

-  什么是window对象? 什么是document对象?

-  null，undefined的区别？

-  写一个通用的事件侦听器函数(机试题)。

-  ["1", "2", "3"].map(parseInt) 答案是多少？

-  关于事件，IE与火狐的事件机制有什么区别？ 如何阻止冒泡？

-  什么是闭包（closure），为什么要用它？

-  javascript 代码中的"use strict";是什么意思 ? 使用它区别是什么？

-  如何判断一个对象是否属于某个类？

-  new操作符具体干了什么呢?

-  用原生JavaScript的实现过什么功能吗？

-  Javascript中，有一个函数，执行时对象查找时，永远不会去查找原型，这个函数是？

-  对JSON的了解？

-  `[].forEach.call($$("*"),function(a){
  a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)
})` 能解释一下这段代码的意思吗？

-  js延迟加载的方式有哪些？

-  Ajax 是什么? 如何创建一个Ajax？

-  同步和异步的区别?

-  如何解决跨域问题?

-  页面编码和被请求的资源编码如果不一致如何处理？

-  服务器代理转发时，该如何处理cookie？

-  模块化开发怎么做？

-  AMD（Modules/Asynchronous-Definition）、CMD（Common Module Definition）规范区别？

-  requireJS的核心原理是什么？（如何动态加载的？如何避免多次加载的？如何
缓存的？）

-  JS模块加载器的轮子怎么造，也就是如何实现一个模块加载器？

-  谈一谈你对ECMAScript6的了解？

-  ECMAScript6 怎么写class，为什么会出现class这种东西?

-  异步加载的方式有哪些？

-  documen.write和 innerHTML的区别?

-  DOM操作——怎样添加、移除、移动、复制、创建和查找节点?

-  .call() 和 .apply() 的作用和区别？

-  数组和对象有哪些原生方法，列举一下？

-  JS 怎么实现一个类。怎么实例化这个类

-  JavaScript中的作用域与变量声明提升？

-  如何编写高性能的Javascript？

-  那些操作会造成内存泄漏？

-  需求：实现一个页面操作不会整页刷新的网站，并且能在浏览器前进、后退时正确响应。给出你的技术实现方案？

-  如何判断当前脚本运行在浏览器还是node环境中？（阿里）

-  移动端最小触控区域是多大？

-  把 Script 标签 放在页面的最底部的body封闭之前 和封闭之后有什么区别？浏览器会如何解析它们？

-  移动端的点击事件的有延迟，时间是多久，为什么会有？ 怎么解决这个延时？（click 有 300ms 延迟,为了实现safari的双击事件的设计，浏览器要知道你是不是要双击操作。）

-  Node.js的适用场景？

-  (如果会用node)知道route, middleware, cluster, nodemon, pm2, server-side rendering么?
-  什么是“前端路由”?什么时候适合使用“前端路由”? “前端路由”有哪些优点和缺点?

-  知道什么是webkit么? 知道怎么用浏览器的各种工具来调试和debug代码么?

- 如何测试前端代码么? 知道BDD, TDD, Unit Test么? 知道怎么测试你的前端工程么(mocha, sinon, jasmin, qUnit..)?

- 用js实现千位分隔符?(来源：[前端农民工](http://div.io/topic/744)，提示：正则+replace)

- What is a Polyfill? 

- 做的项目中，有没有用过或自己实现一些 polyfill 方案（兼容性处理方案）？

- 我们给一个dom同时绑定两个点击事件，一个用捕获，一个用冒泡。会执行几次事件，会先执行冒泡还是捕获？

- 使用JS实现获取文件扩展名？

- Webpack热更新实现原理?

- 请介绍一下JS之事件节流？

- 什么是JS的函数防抖？

- 说说 Promise.all、allSettled、race、any 的区别？

- async/await 的错误处理怎么写更优雅？每段都 try/catch 还是统一封装，你怎么选？

- 事件循环：给一段代码说输出顺序（宏任务/微任务综合变体题，现在基本都是这种考法）。

- Proxy 和 Reflect 的应用场景？Vue3 响应式为什么从 defineProperty 换成 Proxy？

- WeakMap 和 Map 的区别？举一个 WeakMap 的真实使用场景？

- structuredClone() 和 JSON.parse(JSON.stringify()) 深拷贝的区别？

- for...of、for...in、forEach 的区别？Iterator 遍历协议是怎样的？

- Top-level await 的适用场景和坑？

- requestAnimationFrame 和 requestIdleCallback 的区别？长任务怎么拆分避免掉帧？

- 前端内存泄漏现在怎么排查？Chrome DevTools Memory 堆快照用过吗？

- 手写题：防抖、节流、深拷贝、Promise 并发控制、数组扁平化、LRU、柯里化，现在面试怎么考？（更多是结合真实场景，不是干背）

- 事件循环：setTimeout / requestAnimationFrame / queueMicrotask / MessageChannel / requestIdleCallback 的触发时机和优先级，怎么排？

- 设计模式在前端还剩多少价值？说说发布订阅、观察者、策略、代理在现代代码里的真实位置。

- 海量数据的展示和处理：虚拟列表之外还有哪些手段？Web Worker + OffscreenCanvas 能组合出什么？

- WebSocket 之外，实时 Web 还有哪些选型？SSE、WebTransport、Long polling 现在各自的位置。

- performance.mark / measure 和 User Timing API 怎么接入业务监控？和 PerformanceObserver 什么关系？

- WeakMap / WeakSet / FinalizationRegistry 的真实用途是什么？内存调试怎么做？

- __proto__ 是 ES 规范定义的吗？规范获取原型应该用什么？（米哈游面经）

- 为什么基础类型在栈、对象在堆？堆和栈的分工到底是什么？（米哈游面经）

- eval 和 new Function 的区别？你会优先选哪个？（Shopee面经）

- Promise 构造器里同步 throw，后面的 .catch 能捕获得到吗？（Shopee面经）

- 手写：实现一个第一次挂载不执行的 useEffect？（拼多多面经）

- 给一个 json 描述的虚拟 DOM 对象，怎么实现一个把它还原成真实 DOM 的函数？（拼多多面经）

- 依赖注入（DI）和 IoC 在前端有哪些真实应用？哪些开源项目在用？（QQ音乐/蔚来面经）

#### <a name='other'>ECMAScript6 相关</a>

- Object.is() 与原来的比较操作符“ ===”、“ ==”的区别？ 

- ES6是如何实现编译成ES5的？

- css-loader的原理？


#### <a name='ts'>TypeScript 相关</a>

- type 和 interface 的区别？什么场景必须用其中一个？

- unknown 和 any 的区别？为什么说 any 是类型系统的漏洞？（字节）

- 泛型约束（extends）、条件类型、infer 关键字，举一个实际例子？

- 联合类型、交叉类型、可辨识联合（discriminated union）怎么用？

- satisfies 操作符和 as 断言的区别？（TS 4.9+）

- 手写工具类型：Partial、Pick、Omit、ReturnType，实现过哪几个？

- tsconfig 里 strict、moduleResolution、skipLibCheck、isolatedModules 都是干什么的？

- as const 和 enum，项目里你怎么用？为什么说 enum 现在不太被推荐？

- declare、namespace、declare module 这些"全局声明"语法现在还有用武之地吗？

- 怎么做"没有 any 的 lint 策略"？no-explicit-any 落地时怎么处理第三方库和渐进迁移？

- 类型体操在实际业务里到底用在哪？能举两三个真实场景吗？

- satisfies 到底解决了什么问题？和 as 的区别是什么？为什么需要两个关键字？

- 配置 tsconfig 时，skipLibCheck、forceConsistentCasingInFileNames、isolatedModules、verbatimModuleSyntax 分别防什么问题？

## <a name='framework'>前端框架</a>

- React 使用场景？

- 描述一下React 生命周期

- 实现组件有哪些方式？

- 应该在React生命周期的什么阶段发出ajax请求，为什么？

- shouldComponentUpdate函数有什么作用？

- 当组件的setState函数被调用之后，发生了什么？

- 为什么循环产生的组件中要利用上key这个特殊的prop？

- React-router 路由的实现原理？

- 说说React Native,Weex框架的实现原理？

- 受控组件(Controlled Component)与非受控组件(Uncontrolled Component)的区别

- refs 是什么?

- React为什么自己定义一套事件体系呢，与浏览器原生事件体系有什么关系？

- 什么时候应该选择用class实现一个组件，什么时候用一个函数实现一个组件？

- 什么是HoC（Higher-Order Component）？适用于什么场景？

- 并不是父子关系的组件，如何实现相互的数据通信？

- 用过 React 技术栈中哪些数据流管理库？

- Redux是如何做到可预测呢？

- Redux将React组件划分为哪两种？

- Redux是如何将state注入到React组件上的？

- 请描述一次完整的 Redux 数据流

- React的批量更新机制 BatchUpdates？

- React与Vue，各自的组件更新进行对比，它们有哪些区别？

- React 16/17 之后废弃了哪些生命周期？为什么？新的生命周期有哪些？

- React Hooks 为什么不能写在条件语句里？（调用顺序、链表实现）（字节）

- useEffect 和 useLayoutEffect 的区别？什么场景必须用后者？

- React 的 Fiber 架构解决了什么问题？时间切片是怎么回事？

- 说说 React 并发特性和 useTransition、useDeferredValue？

- React 18 的自动批处理（Automatic Batching）和之前手动 batchUpdates 有什么区别？

- React 19 你用了哪些新特性？use()、Actions、useOptimistic、ref as prop？

- React Server Components（RSC）和传统 SSR 的区别？组件什么时候跑在服务端？

- Next.js App Router 的渲染模式（SSR/SSG/ISR/流式渲染）怎么选？缓存策略踩过坑吗？（阿里）

- 虚拟列表（Virtual List）怎么实现？长列表无限滚动白屏怎么优化？

- Vue3 的 ref 和 reactive 区别？解构为什么会丢失响应性？

- 说说 Vue3 的 Composition API 解决了什么问题？和 React Hooks 思路上的异同？

- Vue3 编译期做了哪些优化？（静态提升、Patch Flags）

- Vue 的 diff 和 React 的 diff 有什么核心区别？（双端比较 vs 最长递增子序列）

- Pinia 相比 Vuex 改进了什么？

- Zustand、Jotai 这类轻量状态库为什么流行？和 Redux 怎么选？

- 你们项目是 React 还是 Vue？重新选型你会怎么选，为什么？



- React 的 key 到底解决什么问题？为什么"用 index 当 key"在列表会重排时是 bug？

- useEffect 的依赖数组为什么这么容易被误用？说说闭包陷阱、effect 触发时机、和"从 Props 派生状态"的关系。

- 状态管理在 2026 年怎么选？Redux/Zustand/Jotai/TanStack Query/Context 各自的定位。

- 组件设计：什么是"受控 vs 非受控"？怎么设计一个两种都支持的组件？

- SSR / RSC / 流式渲染这一堆概念，2026 年 Next.js 项目里到底该怎么理解？

- React hooks 的底层实现原理？为什么多次渲染还能拿回上一个状态？（腾讯/米哈游面经）

- Fiber 节点大概是什么样的结构？为什么它能支持中断渲染？（美团面经）

- setState 是同步还是异步？为什么要批量更新？什么时候需要 flushSync 强制同步？（拼多多面经）

- React 为什么要拆分成 react 和 react-dom 两个包？（QQ音乐面经）

- 你觉得 React 有什么缺点或者设计上值得商榷的地方？（米哈游面经）

- React 中跨组件传值/联动的方案有哪些？差异和适用场景分别是什么？（字节面经）

- zustand 的底层原理是什么？依赖收集和订阅是怎么做的？和 Redux 的本质差异在哪？（字节面经）

- SSR 的原理是什么？服务端渲染完之后，浏览器还要做什么？（字节面经）

- 你在真实项目里做过哪些 React 性能优化？性能瓶颈是怎么定位的？（腾讯面经）

- React 组件报错怎么处理？Error Boundary 捕获不到哪些错误？（米哈游面经）

## <a name='eng'>工程化与构建</a>

- 你为什么从 webpack 迁移到 Vite（或反过来）？Vite 开发环境秒启动的原理？

- Vite 为什么开发用 esbuild、生产构建用 Rollup？Rolldown 了解吗？

- Rspack 和 Turbopack 的定位分别是什么？老 webpack 项目迁移成本主要在哪？（头条）

- Babel 和 SWC 的区别？为什么 SWC 快这么多？

- pnpm 为什么省磁盘、装得快？软链接、硬链接和内容寻址存储讲一下。

- npm / yarn / pnpm 怎么选？lock 文件冲突怎么解决？

- Monorepo 怎么落地？pnpm workspace + Turborepo 用过吗？和 git submodule 什么关系？

- Tree Shaking 的原理？sideEffects 配置不起效通常是什么原因？

- 代码分割有哪些手段？路由懒加载之外还做什么？怎么处理预加载？

- SourceMap 原理？线上报错如何还原堆栈，又不把 map 暴露到公网？

- 前端监控怎么做？JS 异常、性能、用户行为采集，Sentry 用过吗？

- 微前端解决什么问题？qiankun、wujie、Module Federation 的 JS 隔离原理分别是什么？

- 你们的 CI/CD 流程是什么样的？前端发布如何做到秒级回滚？

- CDN 缓存策略怎么定？为什么 index.html 不能强缓存？hash 文件名解决什么问题？

- Docker + Nginx 部署前端，gzip/brotli、缓存、history 路由 fallback 怎么配？

- 包体积优化你做过什么？指标和手段分别说说。（gzip 后体积、依赖分析、按需引入）

- Monorepo 在 2026 年怎么落地？pnpm workspace + Turborepo/Nx 各解决什么，什么时候不该用？

- 前端 CI/CD 现在怎么做才算合理？构建产物、缓存、发布策略、回滚说说。

- 前端监控体系怎么搭？错误监控、性能监控、行为日志三条线分别怎么做？

- 前端测试到底测什么？单测/集成/E2E 的投入产出怎么权衡？

- 依赖治理：你怎么控制一个前端项目的依赖风险？

- webpack 插件机制的原理？你们为什么要自定义 webpack 插件？（字节面经）

- 模块联邦（Module Federation）和 npm 包的区别？为什么它适合微前端做共享？（拼多多面经）

- 性能优化专项交给你，"首屏时间"怎么定义、怎么统计？（字节面经）

- 前端错误监控在什么时机、用什么通道上报？（QQ音乐面经）

- 前端埋点怎么实现？团队里怎么管埋点质量？（字节面经）

## <a name='ai'>AI 时代的Web工程实践</a>

- Workflow 和 Agent 的区别是什么？常见的工作流模式有哪些？（Anthropic 官方总结）

- 什么是上下文工程（context engineering）？为什么说上下文是稀缺资源？compaction、笔记、子 agent 各解决什么问题？

- CLAUDE.md / AGENTS.md 这类规则文件应该写什么、不该写什么？为什么说模型外面那层"壳"（harness）才是工程重心？

- 不同模型工具（Claude Code / Cursor / Codex 等）能力差异很大，同一套工作流怎么做到跨模型一致？

- Claude Code 的 hooks 解决什么问题？和把规则写进 CLAUDE.md 有什么本质区别？权限控制怎么做？

- sub-agents 和 skills 分别解决什么问题？为什么说 sub-agent 的价值是上下文隔离而不是"多几个人"？

- 老仓库/大仓库里让 AI 改代码，怎么避免它乱改？验证手段怎么闭环？

- AI 生成的代码你怎么 review？和 review 人写的代码有什么不同？"测试先行"在 AI 时代为什么反而更重要？

- 团队推 AI 提效，你怎么设计和衡量？说说你对 vibe coding 边界的判断。

- 换模型/换供应商（跨模型工作），web 侧怎么设计抽象层？哪些差异是前端要显式处理的？

- AI 产品的流式响应，web 侧为什么大多用 SSE 而不是 WebSocket？fetch + ReadableStream 怎么实现？为什么不用原生 EventSource？

- 流式输出打字机效果，长列表 + 自动滚动 + 高频更新，前端性能有哪些坑？

- AI 回答的 Markdown 是边生成边到达的，增量渲染有哪些坑？代码块、表格在"半截"状态怎么处理？

- 工具调用过程、思考链（reasoning）要在界面上展示，和模型的输出协议怎么设计？说说 AG-UI 这类事件协议解决什么。

- 生成式 UI（generative UI）是什么？让模型"输出组件"怎么落地？有哪些坑？

- 流式回答未完成用户就刷新了/断网重连了，消息怎么幂等、状态怎么恢复？

- AI 对话产品的性能指标和传统 Web 有什么不同？TTFT、token 成本这些怎么纳入前端视野？

- 会话消息状态在前端怎么管理？以什么为真相源？乐观更新和中断、重新生成这些操作怎么设计？

- AI 生成内容（Markdown/HTML/链接/代码）渲染到页面上，XSS 和 prompt injection 怎么防？

- AI 功能上线后，怎么做可观测性和质量监控？这道题只答接口日志就偏表面，往深挖。

- 哪些 AI 功能必须 human in the loop（人来确认），哪些可以全自动？这个边界怎么定？

- 做一个知识库问答（RAG）产品的前端，有哪些比"接个聊天框"深的点？

- 让 AI 生成整块 UI 时，怎么防止它产出一堆"能跑但不像我们的产品"的代码？

- Prompt / 上下文 / 工具定义这些"AI 侧的资产"，怎么做版本管理和回归？它算不算代码？

- MCP 对前端意味着什么？为什么说它可能重演"接口标准化"？

- AI 产品的成本怎么控？除了"少调用"，前端在成本优化里具体能做什么？

- 面向 C 端的 AI 功能，产品形态上 2026 年有哪些被验证过的模式？

- 基模越来越强，作为工程师你的优势是什么？（2026 AI 编程高频题）

- 你负责的模块里，哪些代码让 AI 写、哪些自己写？判断标准是什么？（2026 AI 编程面经）

- AI 生成的"合理但错误"的代码有什么特征？review 时怎么防？（2026 AI 编程面经）

- AI 生成的代码出了线上 bug，你的处理流程是什么？（2026 AI 编程面经）

- AI 写的代码出了问题，让 AI 自己修也修不好，怎么兜底？（2026 AI 编程面经）

- 团队用 AI 编程，Token 成本怎么控制？（2026 AI 编程面经）

- 用 AI 编程工具，怎么保证不泄露公司代码？（2026 AI 编程面经）

- Agent Skills 是什么？和写一段长 Prompt 有什么本质区别？（2026 AI 编程面经）

- 用 AI IDE（Cursor 一类）长期做大项目，你总结出哪些方法论？（2026 AI 编程面经）

- Claude Code 为什么不用 RAG 检索代码，而是用 grep/glob/read 的 agentic search？（2026 AI 编程面经）

- 拆解一下 Claude Code 的核心工作循环（agent loop）？auto-compact 是怎么回事？（2026 AI 编程面经）

- 什么是 Spec-Driven Development？vibe coding 为什么在交付场景要走向规格、计划、任务、验证？（2026 AI 编程面经）

- vibe coding 在 Git 检查点、数据库变更、线上回滚上有哪些翻车点，怎么防？（2026 AI 编程面经）

- AI 会淘汰初级程序员吗？初级在 AI 时代该建什么能力结构？（2026 高频开放题）

## <a name='other'>其他问题</a>

- 原来公司工作流程是怎么样的，如何与其他人协作的？如何跨部门合作的？

- 你遇到过比较难的技术问题是？你是如何解决的？

- 设计模式 知道什么是singleton, factory, strategy, decrator么?

- 常使用的库有哪些？常用的前端开发工具？开发过什么应用或组件？

- 页面重构怎么操作？

- 列举IE与其他浏览器不一样的特性？

- 什么叫优雅降级和渐进增强？

- 是否了解公钥加密和私钥加密。

- WEB应用从服务器主动推送Data到客户端有那些方式？

- 对Node的优点和缺点提出了自己的看法？

- 你有用过哪些前端性能优化的方法？

- http状态码有那些？分别代表是什么意思？

- 一个页面从输入 URL 到页面加载显示完成，这个过程中都发生了什么？（流程说的越详细越好）

- 部分地区用户反应网站很卡，请问有哪些可能性的原因，以及解决方法？

- 从打开app到刷新出内容，整个过程中都发生了什么，如果感觉慢，怎么定位问题，怎么解决?

- 第一次访问页面中时弹出引导，用户关闭引导，之后再次进入页面时不希望出现引导，如何实现？

- 除了前端以外还了解什么其它技术么？你最最厉害的技能是什么？

- 你用的得心应手用的熟练地编辑器&开发环境是什么样子？

- 对前端界面工程师这个职位是怎么样理解的？它的前景会怎么样？

- 你怎么看待Web App 、hybrid App、Native App？

- 你移动端前端开发的理解？（和 Web 前端开发的主要区别是什么？）

- 产品进行版本升级时，可能发生不兼容性问题，如何提前预防和解决？

- 你对加班的看法？

- 平时如何管理你的项目？

- 说说最近最流行的一些东西吧？常去哪些网站？

- 如何设计突发大规模并发架构？

- 是否了解开源的工具 bower、npm、yeoman、grunt、gulp，一个 npm 的包里的 package.json 具备的必要的字段都有哪些？（名称、版本号，依赖）

- 每个模块的代码结构都应该比较简单，且每个模块之间的关系也应该非常清晰，随着功能和迭代次数越来越多，你会如何去保持这个状态的？

- Git知道branch, diff, merge么?

- 当团队人手不足，把功能代码写完已经需要加班的情况下，你会做前端代码的测试吗？

- 知道什么是SEO并且怎么优化么? 知道各种meta data的含义么?

- 移动端（Android IOS）怎么做好用户体验?

- 简单描述一下你做过的移动APP项目研发流程？

- 你在现在的团队处于什么样的角色，起到了什么明显的作用？

- 你认为怎样才是全端工程师（Full Stack developer）？

- 介绍一个你最得意的作品吧？

- 你有自己的技术博客吗，用了哪些技术？

- 对前端安全有什么看法？

- 是否了解Web注入攻击，说下原理，最常见的两种攻击（XSS 和 CSRF）了解到什么程度？

- 项目中遇到国哪些印象深刻的技术难题，具体是什么问题，怎么解决？。

- 最近在学什么东西？

- 你的优点是什么？缺点是什么？

- 如何管理前端团队?

- 最近在学什么？能谈谈你未来3，5年给自己的规划吗？

- 谈谈 Core Web Vitals 三个指标？为什么 INP 取代了 FID？

- HTTP/1.1、HTTP/2、HTTP/3 的区别？QUIC 解决了什么问题？0-RTT 是什么？

- HTTPS 握手过程讲一下？为什么是非对称加密 + 对称加密的组合？

- 跨域的本质？CORS 的简单请求和预检请求区别？credentials 怎么带？

- CSP（内容安全策略）了解吗？现在防 XSS 的主流手段有哪些？

- 大模型产品的前端形态做过吗？流式输出（SSE / fetch ReadableStream）、打字机效果、Markdown 增量渲染怎么处理？（字节/阿里 AI 方向）

- LLM 输出的 Markdown 渲染有什么 XSS 风险？怎么防？

- 你平时用 AI 编程工具吗（Copilot / Cursor / Claude 类）？它改变了你的工作方式吗？

- 怎么保证 AI 生成代码的质量？Code Review 流程有什么变化？

- 你觉得 AI 时代前端会被替代吗？你的护城河是什么？（几乎必问的开放题）

- BFF / Serverless / Edge Runtime 在前端场景里你用过吗？

- 前端低代码/可视化搭建了解吗？Schema、物料、渲染引擎怎么设计？

- Node.js 现在还有什么存在感？说说你的看法。（BFF、CLI、AI 应用层）



- 讲一个你主导的项目，遇到的最难的技术问题是什么，你怎么解决的？

- 需求频繁变更 / 产品经理朝令夕改，你怎么应对？

- 你怎么做技术方案评审 / 怎么写一份让别人服气的方案？

- 上线出了事故，你的处理流程是怎样的？

- 你怎么衡量前端团队 / 自己这一年的价值？只会写页面怎么体现？

- 你对未来三年的技术趋势怎么看？（考技术视野）

- HTTP/2 的头部压缩 HPACK 是什么？为什么 HTTP/2 仍然存在队头阻塞？（米哈游面经）

- WebSocket 和 HTTP/2 的服务端推送有什么区别？现在 Server Push 还算可用方案吗？（米哈游面经）

- TCP 的拥塞控制是怎么做的？UDP 凭什么快，哪些场景应该选 UDP？（米哈游面经）

- 大文件上传怎么实现：分片、秒传、断点续传？（字节面经经典题）

- 热门充电站同一时段出现大量预约请求，如何防止资源超卖？（阿里云面经）

- B 端和 C 端项目在技术关注点上有什么区别？（阿里面经）

## 有趣的问题


- .A、B两人分别在两座岛上。B生病了，A有B所需要的药。C有一艘小船和一个可以上锁的箱子。C愿意在A和B之间运东西，但东西只能放在箱子里。只要箱子没被上锁，C都会偷走箱子里的东西，不管箱子里有什么。如果A和B各自有一把锁和只能开自己那把锁的钥匙，A应该如何把东西安全递交给B？


	    答案：A把药放进箱子，用自己的锁把箱子锁上。B拿到箱子后，再在箱子上加一把自己的锁。
	    箱子运回A后，A取下自己的锁。箱子再运到B手中时，B取下自己的锁，获得药物。

- Amazon主页的左上角有一个商品分类浏览的下拉菜单 没有延迟，而且子菜单也不会在不应该的时候消失。它是怎样做到这一点的呢？

	 	 答案是通过探测鼠标移动的方向和轨迹，具体查看Khan Academy工程师 Ben Kamens 写的 jQuery插件
![这是 Khan Academy工程师 Ben Kamens 写的 jQuery插件](http://a.36krcnd.com/photo/3f716d75a80cdce23c803fc6f088846e.png)


## <a name='web'>前端学习网站推荐</a>

	1. 极客标签：     http://www.gbtags.com/

	2. 码农周刊：     http://weekly.manong.io/issues/

	3. 前端周刊：     http://www.feweekly.com/issues

	4. 慕课网：       http://www.imooc.com/

	5. div.io：		 http://div.io

	6. Hacker News： https://news.ycombinator.com/news

	7. InfoQ：       http://www.infoq.com/

	8. w3cplus：     http://www.w3cplus.com/

	9. Stack Overflow： http://stackoverflow.com/

	10.w3school：    http://www.w3school.com.cn/

	11.mozilla：     https://developer.mozilla.org/zh-CN/docs/Web/

	12. 掘金：         https://juejin.cn/

	13. web.dev：      https://web.dev/

	14. State of JS：  https://2025.stateofjs.com/

	15. roadmap.sh：   https://roadmap.sh/frontend

	16. GitHub Trending： https://github.com/trending

	（2026 注：上面 1、3、5 号老站点已经关站或多年不更了，先留着当考古；新的优先看 MDN、web.dev 和掘金。）



## <a name='web'>文档推荐</a>


1. [jQuery 基本原理](http://docs.huihoo.com/jquery/jquery-fundamentals/zh-cn/index.html "jQuery 基本原理")

2. [JavaScript 秘密花园](http://bonsaiden.github.io/JavaScript-Garden/zh/)

3. [CSS参考手册](http://css.doyoe.com/)

4. [JavaScript 标准参考教程](http://javascript.ruanyifeng.com/)

5. [ECMAScript 6入门](http://es6.ruanyifeng.com/)

6. [现代 JavaScript 教程](https://zh.javascript.info/)

7. [TypeScript 手册](https://www.typescriptlang.org/docs/handbook/intro.html)

8. [React 新版文档](https://react.dev/)

9. [Vue 3 文档](https://cn.vuejs.org/)

10. [web.dev Learn](https://web.dev/learn/)




**备注：**

	根据自己需要选择性阅读，面试题是对理论知识的总结，让自己学会应该如何表达。

	资料答案不够正确和全面，欢迎欢迎Star和提交issues。

	格式不断修改更新中。

	在 github 项目的右上角，有三个按钮,分别是 watch、star、fork，新来的同学注意不要用错了，无休止的邮件提醒会给你造成不必要的信息干扰。

	当你选择Watching，表示你以后会关注这个项目的全部动态，以后只要这个项目发生变动，被别人提交了pull request、被发起了issue等情况你都会收到邮件通知。

	star相当于是点赞或收藏，方便以后查找。

	fork表示你想要补充完善这个项目的内容。

	更新记录：
	2026-09-22： 网掘 2025-2026 真实大厂面经（腾讯/字节/拼多多/美团/阿里/米哈游/QQ音乐/Shopee/蔚来）和 AI 编程面经，新增 45 道实战题：hooks/Fiber/setState 批处理/zustand/SSR 水合/Error Boundary、webpack 插件、模块联邦、首屏口径、错误监控上报、埋点、HPACK/拥塞控制/大文件上传/防超卖、B 端 C 端对比、vibe coding（优势五件套/Token 成本/代码泄露/Skills/agent loop/SDD）等，全部配答案；
	2026-09-22： 清理淘汰了一批彻底过时的老题和答案（jQuery/Zepto 源码细节、Backbone/Ember/Meteor、Mustache/Handlebars 模板、requireJS/AMD/CMD、applicationCache 离线储存、改密码黄底之类的 trivia），并去掉重复题目；IE、Weex 按“技术史”保留；
	2026-09-22： 新增《AI 时代的Web工程实践》章节；Agent 与 harness（context engineering、CLAUDE.md、hooks、跨模型）、AI 代码质量与 vibe coding、面向用户的 AI 产品（流式/SSE、AG-UI 事件协议、生成式 UI、断线恢复、TTFT、RAG 前端）等题目和答案，Staff 向深度；同时给 HTML/CSS/JS/TypeScript/框架/工程化/业务各方向各补了一批结合原理和真实场景的进阶题；
        2026-09-22： 荒废多年后的大更新；新增 CSS 新特性（嵌套 / :has() / 容器查询）、TypeScript、Vite 与 Rust 工具链、pnpm、React 18/19、Vue 3、Core Web Vitals、HTTP/3、AI 辅助编程等题目和答案；老答案里过时的部分加了批注；
	2018-01-14： 公司在招聘前端，使用react技术栈；借此机会更新一波前端框架相关的题目；
	2016-10-20： 更新一些已被发现的问题。
	2016-03-25： 新增ECMAScript6 相关问题


### 更新时间:  2026-09-22

	资料答案不够正确和全面，欢迎欢迎Star和提交issues。我的微博：http://weibo.com/920802999
