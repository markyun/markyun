# 前端开发面试题

## <a name='preface'>前言</a> ##


[只看问题点这里 ](https://markyun.github.io/2015/Front-end-Developer-Questions/ "Questions")

[看全部问题和答案点这里](https://github.com/markyun/My-blog/tree/master/Front-end-Developer-Questions/Questions-and-Answers "Questions-and-Answers")

本文由我收集总结了一些前端面试题，初学者阅后也要用心钻研其中的原理，重要知识需要系统学习、透彻学习，形成自己的知识链。万不可投机取巧，临时抱佛脚只求面试侥幸混过关是错误的！也是不可能的！不可能的！不可能的！

前端还是一个年轻的行业，新的行业标准， 框架， 库都不断在更新和新增，正如赫门在2015深JS大会上的《前端服务化之路》主题演讲中说的一句话：“每18至24个月，前端都会难一倍”，这些变化使前端的能力更加丰富、创造的应用也会更加完美。所以关注各种前端技术，跟上快速变化的节奏，也是身为一个前端程序员必备的技能之一。

最近也收到许多微博私信的鼓励和更正题目信息，后面会经常更新题目和答案到[github博客](http://markyun.github.io/)。希望前端er达到既能使用也会表达，对理论知识有自己的理解。可根据下面的知识点一个一个去进阶学习，形成自己的职业技能链。

先交代一下：距离上一次更新，居然已经是2018年的事了，中间因为工作和生活的原因荒废了很久，惭愧。这几年前端的变化比预期还快——构建工具从 webpack 一路换到 Vite 和 Rust 工具链，CSS 原生嵌套、:has()、容器查询全都落地了，React 走进了 Hooks 和 Server Components 时代，Vue 3 成了新项目的默认选择，TypeScript 基本是标配；最颠覆的是 AI 已经开始直接参与写代码，"你平时怎么用 Copilot / Cursor 这类工具"快变成面试必问题目了。这一波把题目和答案按当下的实际考法更新了一版；老题目里确实过时的（IE hack、Weex 之类）我没有删，留着当技术史看，读的时候心里有个时间概念就好。

**面试有几点需注意：(来源[寒冬winter](http://weibo.com/wintercn "微博：寒冬winter") 老师，github:@wintercn)**

1. 面试题目： 根据你的等级和职位的变化，入门级到专家级，广度和深度都会有所增加。

1. 题目类型： 理论知识、算法、项目细节、技术视野、开放性题、工作案例。

1. 细节追问： 可以确保问到你开始不懂或面试官开始不懂为止，这样可以大大延展题目的区分度和深度，知道你的实际能力。因为这种知识关联是长时期的学习，临时抱佛脚绝对是记不住的。

1. 回答问题再棒，面试官（可能是你面试职位的直接领导），会考虑我要不要这个人做我的同事？所以态度很重要、除了能做事，还要会做人。（感觉更像是相亲( •̣̣̣̣̣̥́௰•̣̣̣̣̣̥̀ )）

1. 资深的前端开发能把absolute和relative弄混，这样的人不要也罢，因为团队需要的是：你这个人具有可以依靠的才能（靠谱）。


**前端开发所需掌握知识点概要：**

	HTML&CSS：
		对Web标准的理解（结构、表现、行为）、浏览器内核、渲染原理、依赖管理、兼容性、CSS语法、层次关系，常用属性、布局、选择器、权重、盒模型、
		Hack、CSS预处理器、CSS3、Flexbox、CSS Modules、Document flow、BFC、HTML5（离线 & 存储、Histoy,多媒体、WebGL\SVG\Canvas）；		
	JavaScript：
        数据类型、运算、对象、Function、继承、闭包、作用域、事件、Prototype、RegExp、JSON、Ajax、DOM、BOM、
        内存泄漏、跨域、异步请求、模板引擎、模块化、Flux、同构、算法、ECMAScript6、Nodejs、HTTP、

	其他：
        主流框架(React\Vue)、Next.js、微前端、TypeScript、RESTFul、WEB安全、前端工程化(Vite\Rspack\pnpm\Monorepo)、
        依赖管理、性能优化(Core Web Vitals)、HTTP/2\HTTP/3、Nodejs\Bun\Serverless、重构、团队协作、可维护、易用性、
        SEO、UED、前端技术选型、AI辅助编程、AI Agent与Harness、流式内容渲染、快速学习能力等；



作为一名前端工程师，**无论工作年头长短都应该掌握的知识点**：

此条由 王子墨 发表在 [攻城师的实验室](http://lab.yuanwai.wang/)

		1、DOM结构 —— 两个节点之间可能存在哪些关系以及如何在节点之间任意移动。

		2、DOM操作 —— 如何添加、移除、移动、复制、创建和查找节点等。

		3、事件 —— 如何使用事件，以及IE和标准DOM事件模型之间存在的差别。

		4、XMLHttpRequest —— 这是什么、怎样完整地执行一次GET请求、怎样检测错误。

		5、严格模式与混杂模式 —— 如何触发这两种模式，区分它们有何意义。

		6、盒模型 —— 外边距、内边距和边框之间的关系，及IE8以下版本的浏览器中的盒模型

		7、块级元素与行内元素 —— 怎么用CSS控制它们、以及如何合理的使用它们

		8、浮动元素 —— 怎么使用它们、它们有什么问题以及怎么解决这些问题。

		9、HTML与XHTML —— 二者有什么区别，你觉得应该使用哪一个并说出理由。

		10、JSON —— 作用、用途、设计结构。



**备注：**

	根据自己需要选择性阅读，面试题是对理论知识的总结，让自己学会应该如何表达。

	资料答案不够正确和全面，欢迎欢迎Star和提交issues。

	格式不断修改更新中。

	更新记录：
	2026-09-22： 网掘 2025-2026 真实大厂面经（腾讯/字节/拼多多/美团/阿里/米哈游/QQ音乐/Shopee/蔚来）和 AI 编程面经，新增 45 道实战题：hooks/Fiber/setState 批处理/zustand/SSR 水合/Error Boundary、webpack 插件、模块联邦、首屏口径、错误监控上报、埋点、HPACK/拥塞控制/大文件上传/防超卖、B 端 C 端对比、vibe coding（优势五件套/Token 成本/代码泄露/Skills/agent loop/SDD）等，全部配答案；
	2026-09-22： 清理淘汰了一批彻底过时的老题和答案（jQuery/Zepto 源码细节、Backbone/Ember/Meteor、Mustache/Handlebars 模板、requireJS/AMD/CMD、applicationCache 离线储存、改密码黄底之类的 trivia），并去掉重复题目；IE、Weex 按“技术史”保留；
	2026-09-22： 新增《AI 时代的Web工程实践》章节；Agent 与 harness（context engineering、CLAUDE.md、hooks、跨模型）、AI 代码质量与 vibe coding、面向用户的 AI 产品（流式/SSE、AG-UI 事件协议、生成式 UI、断线恢复、TTFT、RAG 前端）等题目和答案，Staff 向深度；同时给 HTML/CSS/JS/TypeScript/框架/工程化/业务各方向各补了一批结合原理和真实场景的进阶题；
        2026-09-22： 荒废多年后的大更新；新增 CSS 新特性（嵌套 / :has() / 容器查询）、TypeScript、Vite 与 Rust 工具链、pnpm、React 18/19、Vue 3、Core Web Vitals、HTTP/3、AI 辅助编程等题目和答案；老答案里过时的部分加了批注；
	2018-01-14： 公司在招聘前端，使用react技术栈；借此机会更新一波前端框架相关的题目；
	2016-10-20： 更新一些已被发现的问题。
	2016-03-25： 新增ECMAScript6 相关问题




## <a name='html'>HTML</a>

- Doctype作用？标准模式与兼容模式各有什么区别?

		（1）、<!DOCTYPE>声明位于HTML文档中的第一行，处于 <html> 标签之前。告知浏览器的解析器用什么文档标准解析这个文档。DOCTYPE不存在或格式不正确会导致文档以兼容模式呈现。

		（2）、标准模式的排版 和JS运作模式都是以该浏览器支持的最高标准运行。在兼容模式中，页面以宽松的向后兼容的方式显示,模拟老式浏览器的行为以防止站点无法工作。

- HTML5 为什么只需要写 `<!DOCTYPE HTML>`？

		 HTML5 不基于 SGML，因此不需要对DTD进行引用，但是需要doctype来规范浏览器的行为（让浏览器按照它们应该的方式来运行）；

		 而HTML4.01基于SGML,所以需要对DTD进行引用，才能告知浏览器文档所使用的文档类型。

- 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？

		首先：CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，如div的display默认值为“block”，则为“块级”元素；span默认display属性值为“inline”，是“行内”元素。

		（1）行内元素有：a b span img input select strong（强调的语气）
		（2）块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p

		（3）常见的空元素：
			<br> <hr> <img> <input> <link> <meta>
			鲜为人知的是：
			<area> <base> <col> <command> <embed> <keygen> <param> <source> <track> <wbr>

		不同浏览器（版本）、HTML4（5）、CSS2等实际略有差异
		参考: http://stackoverflow.com/questions/6867254/browsers-default-css-for-html-elements



- 页面导入样式时，使用link和@import有什么区别？


		（1）link属于XHTML标签，除了加载CSS外，还能用于定义RSS, 定义rel连接属性等作用；而@import是CSS提供的，只能用于加载CSS;

		（2）页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;

		（3）import是CSS2.1 提出的，只在IE5以上才能被识别，而link是XHTML标签，无兼容问题;
		 
		 (4)link支持使用js控制DOM去改变样式，而@import不支持;


- 介绍一下你对浏览器内核的理解？

		主要分成两部分：渲染引擎(layout engineer或Rendering Engine)和JS引擎。
		渲染引擎：负责取得网页的内容（HTML、XML、图像等等）、整理讯息（例如加入CSS等），以及计算网页的显示方式，然后会输出至显示器或打印机。浏览器的内核的不同对于网页的语法解释会有不同，所以渲染的效果也不相同。所有网页浏览器、电子邮件客户端以及其它需要编辑、显示网络内容的应用程序都需要内核。

		JS引擎则：解析和执行javascript来实现网页的动态效果。

		最开始渲染引擎和JS引擎并没有区分的很明确，后来JS引擎越来越独立，内核就倾向于只指渲染引擎。

- 常见的浏览器内核有哪些？

        Trident内核：IE,MaxThon,TT,The World,360,搜狗浏览器等。[又称MSHTML]
		Gecko内核：Netscape6及以上版本，FF,MozillaSuite/SeaMonkey等
		Presto内核：Opera7及以上。      [Opera内核原为：Presto，现为：Blink;]
		Webkit内核：Safari,Chrome等。   [ Chrome的：Blink（WebKit的分支）]

      详细文章：[浏览器内核的解析和对比](http://www.cnblogs.com/fullhouse/archive/2011/12/19/2293455.html)



- html5有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和 HTML5？


		* HTML5 现在已经不是 SGML 的子集，主要是关于图像，位置，存储，多任务等功能的增加。
			  绘画 canvas;
			  用于媒介回放的 video 和 audio 元素;
			  本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失;
	          sessionStorage 的数据在浏览器关闭后自动删除;
			  语意化更好的内容元素，比如 article、footer、header、nav、section;
			  表单控件，calendar、date、time、email、url、search;
			  新的技术webworker, websocket, Geolocation;

		  移除的元素：
			  纯表现的元素：basefont，big，center，font, s，strike，tt，u;
			  对可用性产生负面影响的元素：frame，frameset，noframes；

	    * 支持HTML5新标签：
			 IE8/IE7/IE6支持通过document.createElement方法产生的标签，
		  	 可以利用这一特性让这些浏览器支持HTML5新标签，
          	 浏览器支持新标签后，还需要添加标签默认的样式。

		     当然也可以直接使用成熟的框架、比如html5shim;
			 <!--[if lt IE 9]>
				<script> src="http://html5shim.googlecode.com/svn/trunk/html5.js"</script>
			 <![endif]-->

		* 如何区分HTML5： DOCTYPE声明\新增的结构元素\功能元素


- 简述一下你对HTML语义化的理解？

		用正确的标签做正确的事情。
	    html语义化让页面的内容结构化，结构更清晰，便于对浏览器、搜索引擎解析;
	    即使在没有样式CSS情况下也以一种文档格式显示，并且是容易阅读的;
	    搜索引擎的爬虫也依赖于HTML标记来确定上下文和各个关键字的权重，利于SEO;
	    使阅读源代码的人对网站更容易将网站分块，便于阅读维护理解。



- HTML5的离线储存怎么使用，工作原理能不能解释一下？

		在用户没有与因特网连接时，可以正常访问站点或应用，在用户与因特网连接时，更新用户机器上的缓存文件。
		原理：HTML5的离线存储是基于一个新建的.appcache文件的缓存机制(不是存储技术)，通过这个文件上的解析清单离线存储资源，这些资源就会像cookie一样被存储了下来。之后当网络在处于离线状态下时，浏览器会通过被离线存储的数据进行页面展示。


		如何使用：
		1、页面头部像下面一样加入一个manifest的属性；
		2、在cache.manifest文件的编写离线存储的资源；
			CACHE MANIFEST
			#v0.11
			CACHE:
			js/app.js
			css/style.css
			NETWORK:
			resourse/logo.png
			FALLBACK:
			/ /offline.html
		3、在离线状态时，操作window.applicationCache进行需求实现。

	详细的使用请参考：

	[HTML5 离线缓存-manifest简介](http://yanhaijing.com/html/2014/12/28/html5-manifest/)

	[有趣的HTML5：离线存储](http://segmentfault.com/a/1190000000732617)



- 浏览器是怎么对HTML5的离线储存资源进行管理和加载的呢？

		在线的情况下，浏览器发现html头部有manifest属性，它会请求manifest文件，如果是第一次访问app，那么浏览器就会根据manifest文件的内容下载相应的资源并且进行离线存储。如果已经访问过app并且资源已经离线存储了，那么浏览器就会使用离线的资源加载页面，然后浏览器会对比新的manifest文件与旧的manifest文件，如果文件没有发生改变，就不做任何操作，如果文件改变了，那么就会重新下载文件中的资源并进行离线存储。
		离线的情况下，浏览器就直接使用离线存储的资源。
	详细请参考：[有趣的HTML5：离线存储](http://segmentfault.com/a/1190000000732617)

- 请描述一下 cookies，sessionStorage 和 localStorage 的区别？

		cookie是网站为了标示用户身份而储存在用户本地终端（Client Side）上的数据（通常经过加密）。
		cookie数据始终在同源的http请求中携带（即使不需要），记会在浏览器和服务器间来回传递。
		sessionStorage和localStorage不会自动把数据发给服务器，仅在本地保存。

		存储大小：
			cookie数据大小不能超过4k。
			sessionStorage和localStorage 虽然也有存储大小的限制，但比cookie大得多，可以达到5M或更大。

		有期时间：
	    	localStorage    存储持久数据，浏览器关闭后数据不丢失除非主动删除数据；
        	sessionStorage  数据在当前浏览器窗口关闭后自动删除。
			cookie          设置的cookie过期时间之前一直有效，即使窗口或浏览器关闭

- iframe有那些缺点？

		*iframe会阻塞主页面的Onload事件；
		*搜索引擎的检索程序无法解读这种页面，不利于SEO;

		*iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。

        使用iframe之前需要考虑这两个缺点。如果需要使用iframe，最好是通过javascript
        动态给iframe添加src属性值，这样可以绕开以上两个问题。

- Label的作用是什么？是怎么用的？

		label标签来定义表单控制间的关系,当用户选择该标签时，浏览器会自动将焦点转到和标签相关的表单控件上。

		<label for="Name">Number:</label>
		<input type=“text“name="Name" id="Name"/>

		<label>Date:<input type="text" name="B"/></label>

- HTML5的form如何关闭自动完成功能？

		给不想要提示的 form 或某个 input 设置为 autocomplete=off。


- 如何实现浏览器内多个标签页之间的通信? (阿里)

		WebSocket、SharedWorker；
		也可以调用localstorge、cookies等本地存储方式；

		localstorge另一个浏览上下文里被添加、修改或删除时，它都会触发一个事件，
		我们通过监听事件，控制它的值来进行页面信息通信；
		注意quirks：Safari 在无痕模式下设置localstorge值时会抛出 QuotaExceededError 的异常；

- webSocket如何兼容低浏览器？(阿里)

		Adobe Flash Socket 、
		ActiveX HTMLFile (IE) 、
		基于 multipart 编码发送 XHR 、
		基于长轮询的 XHR

- 页面可见性（Page Visibility API） 可以有哪些用途？

		通过 visibilityState 的值检测页面当前是否可见，以及打开网页的时间等;
		在页面被切换到其他后台进程的时候，自动暂停音乐或视频的播放；


- 如何在页面上实现一个圆形的可点击区域？

		1、map+area或者svg
		2、border-radius
		3、纯js实现 需要求一个点在不在圆上简单算法、获取鼠标坐标等等

- 实现不使用 border 画出1px高的线，在不同浏览器的标准模式与怪异模式下都能保持一致的效果。

		<div style="height:1px;overflow:hidden;background:red"></div>


- 网页验证码是干嘛的，是为了解决什么安全问题。

		区分用户是计算机还是人的公共全自动程序。可以防止恶意破解密码、刷票、论坛灌水；
		有效防止黑客对某一个特定注册用户用特定程序暴力破解方式进行不断的登陆尝试。

- title与h1的区别、b与strong的区别、i与em的区别？

		title属性没有明确意义只表示是个标题，H1则表示层次明确的标题，对页面信息的抓取也有很大的影响；

		strong是标明重点内容，有语气加强的含义，使用阅读设备阅读网络时：<strong>会重读，而<B>是展示强调内容。

		i内容展示为斜体，em表示强调的文本；

		Physical Style Elements -- 自然样式标签
		b, i, u, s, pre
		Semantic Style Elements -- 语义样式标签
		strong, em, ins, del, code
		应该准确使用语义样式标签, 但不能滥用, 如果不能确定时首选使用自然样式标签。

- 谈谈你对 Web Components 的理解？自定义元素、Shadow DOM、HTML Template 分别解决什么问题？

		Web Components 是一组标准的合称：Custom Elements（自定义标签）、Shadow DOM（样式与结构封装隔离）、HTML Template（template 标签声明不渲染的模板片段）。
		价值在于"原生组件"：不依赖框架就能做出可复用、样式封装的组件，跨技术栈团队共享组件时特别有用。
		不过说实话，生产里裸写的场景不多，多数配合 Lit / Stencil 这类库在用；企业内部设计系统如果要跨 React/Vue 复用，Web Components 值得考虑。

- 多标签页之间的状态同步你怎么处理？（storage 事件 / BroadcastChannel / SharedWorker）

		常见三种：
		（1）localStorage 的 storage 事件：一个标签页改 storage，同源其他标签页能收到，最简单，注意只在"其他页"触发；
		（2）BroadcastChannel：专门做同源多上下文（标签页/iframe/worker）之间消息广播的 API，用起来像 EventEmitter，现在首选；
		（3）SharedWorker + 消息通知：能做但复杂，实际用得少。
		另外要是有服务端权威场景（协同编辑之类），直接 WebSocket/SSE 推送，不靠浏览器本地同步。

- cookie、sessionStorage、localStorage、IndexedDB 各自的大小限制和使用场景？大量结构化数据怎么存？

		cookie：4KB 左右，每次同源请求都会带上，只适合放小件（登录态、灰度标识），现在越来越多被 token 放 header 替代；
		sessionStorage：5MB 左右，标签页级，关了就没；
		localStorage：5MB 左右（各浏览器略有差异），同源长期存；
		大量结构化数据（离线包、草稿、列表缓存）用 IndexedDB：配额制的数据库级容量，支持事务和索引，全是异步 API，配合 idb 这类轻库用。
		面试常追问：登录态到底放 cookie 还是 localStorage，本质是 XSS / CSRF 风险的取舍，下面其他问题里有 CORS 专题会串起来。

- Page Lifecycle API（frozen / discarded）了解吗？和页面可见性 API 什么关系？

		Page Visibility（visibilitychange）解决"可见/隐藏"；Page Lifecycle 在其上细分出 frozen、discarded 等状态——移动端浏览器后台页会被冻结以省电。
		实用点：页面进后台就暂停定时器/动画/轮询，恢复时重新校准；埋点场景用 freeze 事件提前结算停留时长，否则统计数据会虚高。

- 移动端 100vh 为什么会被浏览器地址栏遮挡？现在怎么解决？（字节）

		移动浏览器的可视视口随地址栏收起/展开在变化，而 100vh 对应的是 large viewport（地址栏收起时的高度），所以地址栏展开时底部内容会被盖住。
		标准解法是新的动态视口单位：svh / lvh / dvh（small/large/dynamic），dvh 跟随地址栏实时变化，兼容性已经全绿；
		老项目还有 JS 监听 visualViewport 设置 --vh 变量的土办法，能用但会抖。

- 无障碍（A11y）做过吗？ARIA 属性了解多少？语义化标签和 tabindex、focus 顺序的关系？

		核心思路：能用原生语义标签（button、nav、main、label）就不要拿 div + ARIA 凑；键盘可达（focus 顺序合理、Tab 能走完）、对比度达标、图片有 alt。
		ARIA 常用的：role、aria-label、aria-expanded、aria-live（动态内容播报，弹窗/异步列表基本必配）；注意 ARIA 只影响"读屏软件听到什么"，不改变行为，aria-disabled 和 disabled 行为就不一样。
		tabindex="0" 加入 Tab 顺序，"-1" 表示只能 JS 聚焦；正值会打乱自然顺序，基本别用。
		现在出海项目和大厂的验收普遍带 a11y 门禁（axe / Lighthouse），它不再是加分项，是及格线。

- 首屏体验现在用什么指标度量？（FCP / LCP / INP / CLS）

		onLoad / DOMContentLoaded 只代表资源加载完，不代表用户"看到了/能用了"。现在标准答案是 Core Web Vitals：
		LCP（最大内容绘制，<=2.5s 良好）、INP（交互到下一帧，2024 年取代了 FID，<=200ms）、CLS（布局偏移，<=0.1）；辅助看 FCP、TTFB。
		实验室数据用 Lighthouse，线上真实用户用 web-vitals 库做 RUM 采集。详细优化抓手在"其他问题"里的 CWV 专题。


- iframe 现在还有哪些合理的使用场景？跨 iframe 通信怎么做？sandbox 属性有哪些坑？

		合理场景就几类：承载第三方隔离内容（地图、支付、视频嵌入）、沙箱化渲染不可信 HTML（用户输入或 AI 生成的富文本，这比前端 sanitize 更彻底）、微前端早期的隔离方案；		通信：postMessage 是唯一正路（targetOrigin 必须写死，写 * 等于裸奔）；同域下 parent 直接操作是历史包袱；		坑：allow-scripts + allow-same-origin 同时开等于没有沙箱（iframe 能自己去掉 sandbox 属性）；sandbox 会禁掉表单提交、弹窗、同源策略，逐项要试；现代配套是 credentialless 和 allow= 属性做细粒度权限。

- 浏览器的存储方案怎么选？Cookie / localStorage / sessionStorage / IndexedDB / Cache Storage，各自的边界和坑。

		先按用途分：登录凭证只能是 Cookie（HttpOnly + Secure + SameSite，防 XSS 偷 cookie 靠 HttpOnly，防 CSRF 靠 SameSite）；轻量配置用 localStorage；单会话状态用 sessionStorage（刷新在、关标签没）；结构化大数据和离线优先 IndexedDB（async API、支持事务、配额按域共享）；静态资源缓存控制用 Cache Storage（SW 里手动管理）；		典型坑：localStorage 存 token 被 XSS 一锅端；localStorage 是同步 API 大数据量卡主线程；Safari ITP 把跨站 cookie 和部分存储当临时数据处理（7 天）；无痕模式下配额骤降；		答题时给出"没有万能方案，按数据敏感度和生命周期选"这个判断力就行。

- 从输入 URL 到页面完全展示，中间都经历了哪些过程？

		DNS（HTTPDNS/DoH）-> TCP 或 QUIC 握手（HTTP/3 的 0-RTT）-> TLS（会话恢复）-> 浏览器侧：HTML 解析、预扫描器提前发起资源请求、关键路径 CSS/JS 阻塞规则、渲染流水线（style/layout/paint/composite）；		2026 年必须补的几段：资源优先级（fetchpriority、importance、preload 的真实作用）、数据获取 waterfall（接口串行等 TTFB 才是多数页面慢的主因，不是网络链路）、hydration/水合成本（框架时代的首屏"可交互"和"看起来好"是两回事）、Core Web Vitals 的度量点（LCP 元素怎么被选出来、INP 的三段耗时）；		这题是面试官的"分辨器"：背旧答案的人讲到 TCP 三次握手就停了，真理解的人讲到水合和指标。

- Web Worker 现在能干什么？SharedArrayBuffer + Atomics 解决了什么问题？什么场景值得上 Worker？

		Worker 解决"主线程被计算霸占"：解析大 JSON、数据处理、搜索索引构建、加解密、AI 推理（onnxruntime-web / transformers.js 都在 Worker/WebGPU 里跑）；		SharedArrayBuffer + Atomics 是质变：线程间共享内存 + 原子操作，不用每条消息序列化拷贝，多线程协作（如 wasm 多线程、并发任务调度）才真正可行；代价是安全门槛——必须隔离跨源嵌入（COOP/COEP 响应头），因为它是侧信道攻击（Spectre）的载体；		上 Worker 的判断：任务 >50ms 量级且可中断（能取消、能上报进度）才值得，通信成本要算账——大对象传 transferable 转移所有权，别结构化克隆拷贝。

- 剪贴板的现代 API 怎么用？和老 execCommand 比好在哪？权限怎么申请？

		新方案是 navigator.clipboard 异步 API：write/read 带 DataItem，支持富内容和文件（截图直接粘成图片），read 需要用户手势 + 权限（ClipboardReader 权限提示），write 在焦点内可直写；老 execCommand('copy') 已废弃，同步阻塞、选择 hack 脆弱、格式单一；		体验细节：粘贴目标识别（读 text/plain 还是 image/png 先判类型再分支）、降级路径（权限被拒引导用户手动 Ctrl+V）、Safari 的焦点沙箱要求（必须在用户手势同步栈内发起）；		富文本编辑器场景还要主动 normalize 粘贴内容——剪贴板是 XSS 和脏数据的入口，先清洗再入模型。

- 图片懒加载怎么实现？C 端项目里你会关注哪些细节？（米哈游面经）

		实现两条路：IntersectionObserver 监听进视口再换 src（threshold / rootMargin 做预加载量），老的 scroll + getBoundingClientRect 节流方案基本可以淘汰了；现在更进一步直接用原生 loading="lazy"，浏览器帮你做视口预估和加载调度；
		C 端的细节比"换 src"多：占位尺寸必须写死或用 aspect-ratio，否则图片一加载就布局偏移、CLS 直接爆；解码用 decoding="async" 不阻塞渲染帧；配合 srcset/sizes 按 DPR 和视口出图，省流量还保清晰；
		再深一层是策略问题：首屏关键图（往往就是 LCP 元素）反而不能懒加载，要 fetchpriority="high" 甚至 preload；真实项目里最常见的负优化就是懒加载规则误伤了 LCP 大图，这条边界说不出来，说明没真上过 C 端；

- 从输入域名到拿到 IP，DNS 的完整查询链路？HTTPS 时代 SNI 还有什么隐私问题？（米哈游面经）

		查询顺序：浏览器 DNS 缓存 → 操作系统（hosts 文件 / 系统缓存）→ 本地递归解析器（运营商或 DoH 服务）→ 递归器从根域名服务器逐层问到顶级域、权威服务器拿 A/AAAA 记录，每一跳都受 TTL 控制；
		光背链路不够，追问都在细节上：A 和 AAAA 是两条独立查询、Happy Eyeballs 会并发择优；CNAME 链有多长影响最终解析耗时；移动弱网下 DNS 占总耗时比例高，所以才有 HTTPDNS、DoH/DoQ 这些绕开运营商 LocalDNS 的方案；
		SNI 这段是 2025 之后的新考点：明文 TLS 握手的 ClientHello 里带着目标域名，中间链路能看你访问谁；解法是 ECH（Encrypted Client Hello）把 SNI 加密进扩展，目前浏览器和云厂商在逐步铺开；

## <a name='css'>CSS</a>

- 介绍一下标准的CSS的盒子模型？低版本IE的盒子模型有什么不同的？

		（1）有两种， IE 盒子模型、W3C 盒子模型；
		（2）盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border)；
		（3）区  别： IE的content部分把 border 和 padding计算了进去;



- CSS选择符有哪些？哪些属性可以继承？

		*   1.id选择器（ # myid）
			2.类选择器（.myclassname）
			3.标签选择器（div, h1, p）
			4.相邻选择器（h1 + p）
			5.子选择器（ul > li）
			6.后代选择器（li a）
			7.通配符选择器（ * ）
			8.属性选择器（a[rel = "external"]）
			9.伪类选择器（a:hover, li:nth-child）

		*   可继承的样式： font-size font-family color, UL LI DL DD DT;

		*   不可继承的样式：border padding margin width height ;



- CSS优先级算法如何计算？

		*   优先级就近原则，同权重情况下样式定义最近者为准;
		*   载入样式以最后载入的定位为准;

		优先级为:
			同权重: 内联样式表（标签内部）> 嵌入样式表（当前文件中）> 外部样式表（外部文件中）。
			!important >  id > class > tag
			important 比 内联优先级高

- CSS3新增伪类有那些？

			举例：
			p:first-of-type	选择属于其父元素的首个 <p> 元素的每个 <p> 元素。
			p:last-of-type	选择属于其父元素的最后 <p> 元素的每个 <p> 元素。
	        p:only-of-type	选择属于其父元素唯一的 <p> 元素的每个 <p> 元素。
			p:only-child		选择属于其父元素的唯一子元素的每个 <p> 元素。
			p:nth-child(2)	选择属于其父元素的第二个子元素的每个 <p> 元素。

			::after			在元素之前添加内容,也可以用来做清除浮动。
			::before			在元素之后添加内容
	 	    :enabled  		
			:disabled 		控制表单控件的禁用状态。
			:checked        单选框或复选框被选中。

- 如何居中div？


	*  水平居中：给div设置一个宽度，然后添加margin:0 auto属性

			div{
				width:200px;
				margin:0 auto;
			 }

	*  让绝对定位的div居中

			div {
				position: absolute;
				width: 300px;
				height: 300px;
				margin: auto;
				top: 0;
				left: 0;
				bottom: 0;
				right: 0;
				background-color: pink;	/* 方便看效果 */
			}

	*  水平垂直居中一

			确定容器的宽高 宽500 高 300 的层
			设置层的外边距

			div {
				position: relative;		/* 相对定位或绝对定位均可 */
				width:500px;
				height:300px;
				top: 50%;
				left: 50%;
				margin: -150px 0 0 -250px;     	/* 外边距为自身宽高的一半 */
				background-color: pink;	 	/* 方便看效果 */

			 }

	*  水平垂直居中二

			未知容器的宽高，利用 `transform` 属性

			div {
				position: absolute;		/* 相对定位或绝对定位均可 */
				width:500px;
				height:300px;
				top: 50%;
				left: 50%;
				transform: translate(-50%, -50%);
				background-color: pink;	 	/* 方便看效果 */

			}

	*  水平垂直居中三

			利用 flex 布局
			实际使用时应考虑兼容性

			.container {
				display: flex;
				align-items: center; 		/* 垂直居中 */
				justify-content: center;	/* 水平居中 */

			}
			.container div {
				width: 100px;
				height: 100px;
				background-color: pink;		/* 方便看效果 */
			}  


- display有哪些值？说明他们的作用。

		  block       	块类型。默认宽度为父元素宽度，可设置宽高，换行显示。
		  none        	元素不显示，并从文档流中移除。
		  inline      	行内元素类型。默认宽度为内容宽度，不可设置宽高，同行显示。
		  inline-block  默认宽度为内容宽度，可以设置宽高，同行显示。
		  list-item   	象块类型元素一样显示，并添加样式列表标记。
		  table       	此元素会作为块级表格来显示。
		  inherit     	规定应该从父元素继承 display 属性的值。


- position的值relative和absolute定位原点是？

		  absolute
			生成绝对定位的元素，相对于值不为 static的第一个父元素进行定位。
		  fixed （老IE不支持）
			生成绝对定位的元素，相对于浏览器窗口进行定位。
		  relative
			生成相对定位的元素，相对于其正常位置进行定位。
		  static
			默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right z-index 声明）。
		  inherit
			规定从父元素继承 position 属性的值。

- CSS3有哪些新特性？

		  新增各种CSS选择器	（: not(.input)：所有 class 不是“input”的节点）
  		  圆角		    （border-radius:8px）
		  多列布局	    （multi-column layout）
		  阴影和反射	（Shadow\Reflect）
		  文字特效		（text-shadow、）
		  文字渲染		（Text-decoration）
		  线性渐变		（gradient）
		  旋转		 	（transform）
          缩放,定位,倾斜,动画,多背景
		  例如:transform:\scale(0.85,0.90)\ translate(0px,-30px)\ skew(-9deg,0deg)\Animation:

- 请解释一下CSS3的Flexbox（弹性盒布局模型）,以及适用场景？

		 一个用于页面布局的全新CSS3功能，Flexbox可以把列表放在同一个方向（从上到下排列，从左到右），并让列表能延伸到占用可用的空间。
		 较为复杂的布局还可以通过嵌套一个伸缩容器（flex container）来实现。
		 采用Flex布局的元素，称为Flex容器（flex container），简称"容器"。
		 它的所有子元素自动成为容器成员，称为Flex项目（flex item），简称"项目"。
		 常规布局是基于块和内联流方向，而Flex布局是基于flex-flow流可以很方便的用来做局中，能对不同屏幕大小自适应。
		 在布局上有了比以前更加灵活的空间。

		 具体：http://www.w3cplus.com/css3/flexbox-basics.html

- 用纯CSS创建一个三角形的原理是什么？

		把上、左、右三条边隐藏掉（颜色设为 transparent）
		#demo {
		  width: 0;
		  height: 0;
		  border-width: 20px;
		  border-style: solid;
		  border-color: transparent transparent red transparent;
		}

- 一个满屏 品 字布局 如何设计?

		简单的方式：
			上面的div宽100%，
			下面的两个div分别宽50%，
			然后用float或者inline使其不换行即可

- css多列等高如何实现？

		利用padding-bottom|margin-bottom正负值相抵；
		设置父容器设置超出隐藏（overflow:hidden），这样子父容器的高度就还是它里面的列没有设定padding-bottom时的高度，
		当它里面的任 一列高度增加了，则父容器的高度被撑到里面最高那列的高度，
		其他比这列矮的列会用它们的padding-bottom补偿这部分高度差。


- 经常遇到的浏览器的兼容性有哪些？原因，解决方法是什么，常用hack的技巧 ？

	    * png24位的图片在iE6浏览器上出现背景，解决方案是做成PNG8.

		* 浏览器默认的margin和padding不同。解决方案是加一个全局的*{margin:0;padding:0;}来统一。

		* IE6双边距bug:块属性标签float后，又有横行的margin情况下，在ie6显示margin比设置的大。

		  浮动ie产生的双倍距离 #box{ float:left; width:10px; margin:0 0 0 100px;}

	      这种情况之下IE会产生20px的距离，解决方案是在float的标签样式控制中加入 ——_display:inline;将其转化为行内属性。(_这个符号只有ie6会识别)

		  渐进识别的方式，从总体中逐渐排除局部。

		  首先，巧妙的使用“\9”这一标记，将IE游览器从所有情况中分离出来。
		  接着，再次使用“+”将IE8和IE7、IE6分离开来，这样IE8已经独立识别。

          css
	          .bb{
		          background-color:red;/*所有识别*/
			      background-color:#00deff\9; /*IE6、7、8识别*/
			      +background-color:#a200ff;/*IE6、7识别*/
			      _background-color:#1e0bd1;/*IE6识别*/
	          }


		*  IE下,可以使用获取常规属性的方法来获取自定义属性,
		   也可以使用getAttribute()获取自定义属性;
           Firefox下,只能使用getAttribute()获取自定义属性。
           解决方法:统一通过getAttribute()获取自定义属性。

		*  IE下,even对象有x,y属性,但是没有pageX,pageY属性;
           Firefox下,event对象有pageX,pageY属性,但是没有x,y属性。

		*  解决方法：（条件注释）缺点是在IE浏览器下可能会增加额外的HTTP请求数。

		*  Chrome 中文界面下默认会将小于 12px 的文本强制按照 12px 显示,
		   可通过加入 CSS 属性 -webkit-text-size-adjust: none; 解决。

		超链接访问过后hover样式就不出现了 被点击访问过的超链接样式不在具有hover和active了解决方法是改变CSS属性的排列顺序:
	    L-V-H-A :  a:link {} a:visited {} a:hover {} a:active {}


- li与li之间有看不见的空白间隔是什么原因引起的？有什么解决办法？

		行框的排列会受到中间空白（回车\空格）等的影响，因为空格也属于字符,这些空白也会被应用样式，占据空间，所以会有间隔，把字符大小设为0，就没有空格了。


- 为什么要初始化CSS样式。

		- 因为浏览器的兼容问题，不同浏览器对有些标签的默认值是不同的，如果没对CSS初始化往往会出现浏览器之间的页面显示差异。

		- 当然，初始化样式会对SEO有一定的影响，但鱼和熊掌不可兼得，但力求影响最小的情况下初始化。

		最简单的初始化方法： * {padding: 0; margin: 0;} （强烈不建议）

		淘宝的样式初始化代码：
		body, h1, h2, h3, h4, h5, h6, hr, p, blockquote, dl, dt, dd, ul, ol, li, pre, form, fieldset, legend, button, input, textarea, th, td { margin:0; padding:0; }
		body, button, input, select, textarea { font:12px/1.5tahoma, arial, \5b8b\4f53; }
		h1, h2, h3, h4, h5, h6{ font-size:100%; }
		address, cite, dfn, em, var { font-style:normal; }
		code, kbd, pre, samp { font-family:couriernew, courier, monospace; }
		small{ font-size:12px; }
		ul, ol { list-style:none; }
		a { text-decoration:none; }
		a:hover { text-decoration:underline; }
		sup { vertical-align:text-top; }
		sub{ vertical-align:text-bottom; }
		legend { color:#000; }
		fieldset, img { border:0; }
		button, input, select, textarea { font-size:100%; }
		table { border-collapse:collapse; border-spacing:0; }


- absolute的containing block(容器块)计算方式跟正常流有什么不同？

		无论属于哪种，都要先找到其祖先元素中最近的 position 值不为 static 的元素，然后再判断：
		1、若此元素为 inline 元素，则 containing block 为能够包含这个元素生成的第一个和最后一个 inline box 的 padding box (除 margin, border 外的区域) 的最小矩形；
		2、否则,则由这个祖先元素的 padding box 构成。
		如果都找不到，则为 initial containing block。

		补充：
		1. static(默认的)/relative：简单说就是它的父元素的内容框（即去掉padding的部分）
		2. absolute: 向上找最近的定位为absolute/relative的元素
		3. fixed: 它的containing block一律为根元素(html/body)，根元素也是initial containing block

- CSS里的visibility属性有个collapse属性值是干嘛用的？在不同浏览器下以后什么区别？

	对于普通元素visibility:collapse;会将元素完全隐藏,不占据页面布局空间,与display:none;表现相同.
	如果目标元素为table,visibility:collapse;将table隐藏,但是会占据页面布局空间.
	仅在Firefox下起作用,IE会显示元素,Chrome会将元素隐藏,但是占据空间.

- position跟display、margin collapse、overflow、float这些特性相互叠加后会怎么样？

	如果元素的display为none,那么元素不被渲染,position,float不起作用,如果元素拥有position:absolute;或者position:fixed;属性那么元素将为绝对定位,float不起作用.如果元素float属性不是none,元素会脱离文档流,根据float属性值来显示.有浮动,绝对定位,inline-block属性的元素,margin不会和垂直方向上的其他元素margin折叠.
	
- 对BFC规范(块级格式化上下文：block formatting context)的理解？

		（W3C CSS 2.1 规范中的一个概念,它是一个独立容器，决定了元素如何对其内容进行定位,以及与其他元素的关系和相互作用。）
		 一个页面是由很多个 Box 组成的,元素的类型和 display 属性,决定了这个 Box 的类型。
		 不同类型的 Box,会参与不同的 Formatting Context（决定如何渲染文档的容器）,因此Box内的元素会以不同的方式渲染,也就是说BFC内部的元素和外部的元素不会互相影响。

- css定义的权重

		以下是权重的规则：标签的权重为1，class的权重为10，id的权重为100，以下例子是演示各种定义的权重值：

		/*权重为1*/
		div{
		}
		/*权重为10*/
		.class1{
		}
		/*权重为100*/
		#id1{
		}
		/*权重为100+1=101*/
		#id1 div{
		}
		/*权重为10+1=11*/
		.class1 div{
		}
		/*权重为10+10+1=21*/
		.class1 .class2 div{
		}

		如果权重相同，则最后定义的样式会起作用，但是应该避免这种情况出现


- 请解释一下为什么需要清除浮动？清除浮动的方式

	清除浮动是为了清除使用浮动元素产生的影响。浮动的元素，高度会塌陷，而高度的塌陷使我们页面后面的布局不能正常显示。

		1、父级div定义height；
		2、父级div 也一起浮动；
		3、常规的使用一个class；
			.clearfix::before, .clearfix::after {
			    content: " ";
			    display: table;
			}
			.clearfix::after {
			    clear: both;
			}
			.clearfix {
			    *zoom: 1;
			}

		4、SASS编译的时候，浮动元素的父级div定义伪类:after
			&::after,&::before{
			    content: " ";
		        visibility: hidden;
		        display: block;
		        height: 0;
		        clear: both;
			}

		解析原理：
		1) display:block 使生成的元素以块级元素显示,占满剩余空间;
		2) height:0 避免生成内容破坏原有布局的高度。
		3) visibility:hidden 使生成的内容不可见，并允许可能被生成内容盖住的内容可以进行点击和交互;
		4）通过 content:"."生成内容作为最后一个元素，至于content里面是点还是其他都是可以的，例如oocss里面就有经典的 content:".",有些版本可能content 里面内容为空,一丝冰凉是不推荐这样做的,firefox直到7.0 content:”" 仍然会产生额外的空隙；
		5）zoom：1 触发IE hasLayout。

		通过分析发现，除了clear：both用来闭合浮动的，其他代码无非都是为了隐藏掉content生成的内容，这也就是其他版本的闭合浮动为什么会有font-size：0，line-height：0。

- 什么是外边距合并？

		外边距合并指的是，当两个垂直外边距相遇时，它们将形成一个外边距。
		合并后的外边距的高度等于两个发生合并的外边距的高度中的较大者。
		w3school介绍网址： http://www.w3school.com.cn/css/css_margin_collapsing.asp

- zoom:1的清除浮动原理?

		清除浮动，触发hasLayout；
		Zoom属性是IE浏览器的专有属性，它可以设置或检索对象的缩放比例。解决ie下比较奇葩的bug。
		譬如外边距（margin）的重叠，浮动清除，触发ie的haslayout属性等。

		来龙去脉大概如下：
		当设置了zoom的值之后，所设置的元素就会就会扩大或者缩小，高度宽度就会重新计算了，这里一旦改变zoom值时其实也会发生重新渲染，运用这个原理，也就解决了ie下子元素浮动时候父元素不随着自动扩大的问题。

		Zoom属是IE浏览器的专有属性，火狐和老版本的webkit核心的浏览器都不支持这个属性。然而，zoom现在已经被逐步标准化，出现在 CSS 3.0 规范草案中。

		目前非ie由于不支持这个属性，它们又是通过什么属性来实现元素的缩放呢？
		可以通过css3里面的动画属性scale进行缩放。

- 移动端的布局用过媒体查询吗？


	假设你现在正用一台显示设备来阅读这篇文章，同时你也想把它投影到屏幕上，或者打印出来，
	而显示设备、屏幕投影和打印等这些媒介都有自己的特点，CSS就是为文档提供在不同媒介上展示的适配方法

	<!-- link元素中的CSS媒体查询 -->
	当媒体查询为真时，相关的样式表或样式规则会按照正常的级联规被应用。
	当媒体查询返回假， <link> 标签上带有媒体查询的样式表 仍将被下载 （只不过不会被应用）。

	<link rel="stylesheet" media="(max-width: 800px)" href="example.css" />

	<!-- 样式表中的CSS媒体查询 -->
	包含了一个媒体类型和至少一个使用 宽度、高度和颜色等媒体属性来限制样式表范围的表达式。
	CSS3加入的媒体查询使得无需修改内容便可以使样式应用于某些特定的设备范围。

	<style>
		@media (min-width: 700px) and (orientation: landscape){
		  .sidebar {
		    display: none;
		  }
		}
	</style>



- 使用 CSS 预处理器吗？喜欢那个？

		SASS (SASS、LESS没有本质区别，只因为团队前端都是用的SASS)


- CSS优化、提高性能的方法有哪些？

		关键选择器（key selector）。选择器的最后面的部分为关键选择器（即用来匹配目标元素的部分）；
		如果规则拥有 ID 选择器作为其关键选择器，则不要为规则增加标签。过滤掉无关的规则（这样样式系统就不会浪费时间去匹配它们了）；
		提取项目的通用公有样式，增强可复用性，按模块编写组件；增强项目的协同开发性、可维护性和可扩展性;
		使用预处理工具或构建工具（gulp对css进行语法检查、自动补前缀、打包压缩、自动优雅降级）；


- 浏览器是怎样解析CSS选择器的？

		样式系统从关键选择器开始匹配，然后左移查找规则选择器的祖先元素。
		只要选择器的子树一直在工作，样式系统就会持续左移，直到和规则匹配，或者是因为不匹配而放弃该规则。


- 在网页中的应该使用奇数还是偶数的字体？为什么呢？

- margin和padding分别适合什么场景使用？

		margin是用来隔开元素与元素的间距；padding是用来隔开元素与内容的间隔。
		margin用于布局分开元素使元素与元素互不相干；
		padding用于元素与内容之间的间隔，让内容（文字）与（包裹）元素之间有一段


- 抽离样式模块怎么写，说出思路，有无实践经验？[阿里航旅的面试题]

- 元素竖向的百分比设定是相对于容器的高度吗？

- 全屏滚动的原理是什么？用到了CSS的那些属性？

- 什么是响应式设计？响应式设计的基本原理是什么？如何兼容低版本的IE？

- 视差滚动效果，如何给每页做不同的动画？（回到顶部，向下滑动要再次出现，和只出现一次分别怎么做？）

- ::before 和 :after中双冒号和单冒号 有什么区别？解释一下这2个伪元素的作用。

		单冒号(:)用于CSS3伪类，双冒号(::)用于CSS3伪元素。（伪元素由双冒号和伪元素名称组成）
		双冒号是在当前规范中引入的，用于区分伪类和伪元素。不过浏览器需要同时支持旧的已经存在的伪元素写法，
		比如:first-line、:first-letter、:before、:after等，
		而新的在CSS3中引入的伪元素则不允许再支持旧的单冒号的写法。

		想让插入的内容出现在其它内容前，使用::before，否者，使用::after；
		在代码顺序上，::after生成的内容也比::before生成的内容靠后。
		如果按堆栈视角，::after生成的内容会在::before生成的内容之上


- 如何修改chrome记住密码后自动填充表单的黄色背景 ？

		input:-webkit-autofill, textarea:-webkit-autofill, select:-webkit-autofill {
		  background-color: rgb(250, 255, 189); /* #FAFFBD; */
		  background-image: none;
		  color: rgb(0, 0, 0);
		}

- 你对line-height是如何理解的？

- 设置元素浮动后，该元素的display值是多少？

		自动变成了 display:block

- 怎么让Chrome支持小于12px 的文字？

		1、用图片：如果是内容固定不变情况下，使用将小于12px文字内容切出做图片，这样不影响兼容也不影响美观。
		2、使用12px及12px以上字体大小：为了兼容各大主流浏览器，建议设计美工图时候设置大于或等于12px的字体大小，如果是接单的这个时候就需要给客户讲解小于12px浏览器不兼容等事宜。
		3、继续使用小于12px字体大小样式设置：如果不考虑chrome可以不用考虑兼容，同时在设置小于12px对象设置-webkit-text-size-adjust:none，做到最大兼容考虑。
		4、使用12px以上字体：为了兼容、为了代码更简单 从新考虑权重下兼容性。

- 让页面里的字体变清晰，变细用CSS怎么做？

		-webkit-font-smoothing: antialiased;

- font-style属性可以让它赋值为“oblique” oblique是什么意思？

		倾斜的字体样式

- position:fixed;在android下无效怎么处理？

		fixed的元素是相对整个页面固定位置的，你在屏幕上滑动只是在移动这个所谓的viewport，
		原来的网页还好好的在那，fixed的内容也没有变过位置，
		所以说并不是iOS不支持fixed，只是fixed的元素不是相对手机屏幕固定的。
		<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, user-scalable=no"/>

- 如果需要手动写动画，你认为最小时间间隔是多久，为什么？（阿里）

		多数显示器默认频率是60Hz，即1秒刷新60次，所以理论上最小间隔为1/60＊1000ms ＝ 16.7ms

- display:inline-block 什么时候会显示间隙？(携程)

		移除空格、使用margin负值、使用font-size:0、letter-spacing、word-spacing

- overflow: scroll时不能平滑滚动的问题怎么处理？

- 有一个高度自适应的div，里面有两个div，一个高度100px，希望另一个填满剩下的高度。

- png、jpg、gif 这些图片格式解释一下，分别什么时候用。有没有了解过webp？


- 什么是Cookie 隔离？（或者说：请求资源的时候不要让它带cookie怎么做）

		如果静态文件都放在主域名下，那静态文件请求的时候都带有的cookie的数据提交给server的，非常浪费流量，
		所以不如隔离开。

		因为cookie有域的限制，因此不能跨域提交请求，故使用非主要域名的时候，请求头中就不会带有cookie数据，
		这样可以降低请求头的大小，降低请求时间，从而达到降低整体请求延时的目的。

		同时这种方式不会将cookie传入Web Server，也减少了Web Server对cookie的处理分析环节，
		提高了webserver的http请求的解析速度。


- style标签写在body后与body前有什么区别？


- 什么是CSS 预处理器 / 后处理器？

		- 预处理器例如：LESS、Sass、Stylus，用来预编译Sass或less，增强了css代码的复用性，
		  还有层级、mixin、变量、循环、函数等，具有很方便的UI组件模块化开发能力，极大的提高工作效率。

		- 后处理器例如：PostCSS，通常被视为在完成的样式表中根据CSS规范处理CSS，让其更有效；目前最常做的
		  是给CSS属性添加浏览器私有前缀，实现跨浏览器兼容性的问题。


- rem布局的优缺点

- CSS 原生嵌套（Nesting）和 Less/Sass 的嵌套有什么区别？还需要预处理器吗？

		语法几乎一样，主流浏览器已原生支持（Chrome 112+ / Firefox 117+ / Safari 17.2，更早的 Safari 16.5 为部分支持）。区别在于：
		（1）原生嵌套可以混着 :has()、& 出现在任意位置等预处理器做不到的写法；
		（2）预处理器剩下的价值主要是变量/mixin/函数这些编译期能力，而变量已被 CSS 自定义属性接管，所以占比越来越小；
		趋势是：新项目 CSS 原生嵌套 + 自定义属性就够，Less/Sass 在退场，PostCSS 退居做语法降级（postcss-preset-env）。

- :has() 选择器为什么被称为"父选择器"？举一个你的实际使用场景？

		因为它可以根据后代的状态选中祖先元素：.card:has(img) 选中"里面有图片的卡片"；
		再如 form:has(:invalid) .submit { opacity: .5 }，表单非法时置灰提交按钮，零 JS；
		比 :focus-within 强在能表达任意条件。Safari 15.4 起全部主流浏览器支持，基本能覆盖以前只能靠 JS 加 class 的大多数场景。

- 容器查询（Container Queries）和媒体查询的区别？为什么说它更适合组件化开发？

		媒体查询看"视口"断点；容器查询看"组件所在容器"的尺寸断点（container-type: inline-size + @container）。
		本质区别：组件不再关心"屏幕多宽"，只关心"我被放进多宽的地方"——同一个卡片，侧栏里窄版布局、主区里宽版布局，复用到哪自适应到哪，这才是"组件级响应式"。
		注意两点：容器查询不能查自身，要包一层 container；容器会成为新的 containing block，absolute 定位要留心。

- @layer（层叠层）解决什么问题？和用 !important 硬怼优先级有什么本质区别？

		解决"来源优先级"问题：reset、组件库、业务代码三层样式谁覆盖谁，以前只能靠加载顺序和提权（!important、多加选择器），越怼越乱。
		@layer base, vendor, components, app; 声明一次，层与层的优先级就定死了，跟选择器权重解耦；
		!important 是打破规则，layer 是重写规则——可维护性上后者才是解。Tailwind v4 内部就是用 layer 解决和自定义样式打架的问题。

- CSS 自定义属性（CSS 变量）和预处理器变量的区别？运行时主题切换/暗色模式怎么做？

		预处理器变量编译后就消失了；CSS 变量是活的：挂在 :root 上、可继承、能被 JS setProperty 修改、能被媒体查询覆盖。
		主题切换标准做法：设计 token 定义成变量挂在 :root，暗色主题在 html.dark 下重定义同一批变量（配合 prefers-color-scheme 做默认值），切换只改一个 class，不用刷新不用重编译；
		组件库（antd v5 等）的主题定制也是这套 token 思路。

- color-mix()、oklch() 这些现代颜色函数用过吗？

		oklch 是感知均匀色彩空间，调明度/饱和度生成色阶不会跑偏、色域外问题也少，设计系统用它产主题色阶很顺手（Tailwind v4 已转 oklch）；
		color-mix(in oklab, var(--brand) 10%, white) 可以直接混出 hover 态、浅背景，不用再靠预处理器算色。
		配合 CSS 变量，一套主题基本可以纯 CSS 维护。

- View Transitions API 了解吗？现在做页面/路由转场动画的标准做法是什么？

		浏览器原生的状态转场：document.startViewTransition(() => 改DOM)，浏览器对新旧状态截图，默认 cross-fade，可用 ::view-transition-old/new 自定义动画；
		同文档转场兼容性已经铺开；跨文档（MPA）转场 Chrome 126+ 支持，@view-transition { navigation: auto } 让多页应用也有共享元素动画；
		react-router / Next.js 都接了这个 API。以前要 framer-motion 手工做的转场，现在浏览器原生就能接住。

- 如何看待 Tailwind 这类原子化 CSS？它的优缺点，你们项目里怎么选型？（阿里）

		优点：不用纠结命名、样式结构不分离、构建产物只含用到的类、配合 IDE 提示效率高、设计 token 约束下团队样式一致；
		缺点：模板里 class 一长串可读性差、设计一致性依赖 token 体系本身、非前端同学接手有门槛；
		我的判断：中后台和初创团队 to-C 页面提效明显；强设计驱动的大型项目要看设计系统怎么落地。
		2026 的视角：Tailwind v4 用 Rust 引擎（Oxide）重写，配置从 JS 文件转向 CSS @theme，加上原生嵌套和 layer 落地，原子化和原生 CSS 的边界在变模糊。

- browserslist、autoprefixer、PostCSS 现在的定位发生了什么变化？

		autoprefixer 从前是刚需，现在主流浏览器版本更新快，大量前缀早就不需要了，browserslist 里去掉老浏览器后产物反而更小；
		PostCSS 的重心从"加前缀"转向"语法降级"（postcss-preset-env 把嵌套、:has 降级）；如果 targets 只设近两年的浏览器，这些也基本可以关；
		再一个趋势是 Lightning CSS / Rolldown 把这块内建到构建工具里了。

- 双栏/三栏自适应布局你现在怎么写？（Grid minmax + auto-fit / 容器查询组合拳）

		侧栏固定 + 主区自适应：grid-template-columns: 260px minmax(0, 1fr)（minmax(0,1fr) 防止子项内容撑破轨道，踩过坑的都懂）；
		数量不定的卡片自动换行：repeat(auto-fit, minmax(280px, 1fr))，一行媒体查询都不用写；
		两栏中"一栏固定一栏填满"以前 flex:1 + overflow hidden 也行；复杂杂志排版再看 subgrid。
		float + clearfix 那套就当历史课听吧。




- 深/浅主题切换你怎么架构？next-themes 这类方案的 FOUC 问题怎么解决？

		基础是 CSS 自定义属性做语义化 token（--color-bg、--color-text），主题只切 token 值不切组件——组件永远不感知具体色值；		SSR 场景的 FOUC：服务端不知道用户偏好，先按系统/默认渲染，客户端 hydrate 后读到 localStorage 再切换就闪一下。解法是在 <head> 里放一段阻塞脚本，在首次绘制前同步设置 html 的 data-theme 属性（很小，值得阻塞）；这正是"内联脚本 vs CSP"的冲突点，要么 nonce 豁免要么用媒体查询兜底；		进阶：prefers-color-scheme 做默认值、localStorage 做用户覆盖、watchMedia 监听系统切换（未显式设置时跟随）；三色管理（surface/border/text）比逐色枚举稳定。

- Tailwind 和原生 CSS 增强（嵌套/:has()/容器查询/@layer）都落地了，2026 年 CSS 该怎么选型？

		我的判断标准是人和合作方：设计侧有严格规范、团队流动大、要和设计稿强映射——Tailwind 收益实在（约束即效率）；组件库、小团队、重度动效和精细排版——原生 + 设计 token 更干净，不再需要预处理器全家桶；		关键共识是分层：utility 不是原罪，混乱才是——用 @layer 把 reset/基础/组件/utility 排好层，天然解决优先级打架（这就是 @layer 存在的意义）；		别答成宗教战争，说清楚"按团队和产物形态选，迁移成本计入"就是资深信号。

- 设计系统的前端落地：design token 怎么建模？组件库、主题、文档怎么协作？

		token 分三层：原始值（blue-500）-> 语义值（color-action-primary）-> 组件值（button-bg），组件只消费语义层，改品牌只动映射不动组件；token 源文件用 Style Dictionary 类工具编译成 CSS 变量/各端产物，避免"设计改一笔、前端全网搜"；		配套工程：组件 API 的边界要文档化（什么可覆写、用什么 prop），视觉回归测试接 CI（Chromatic/Playwright 截图比对），可访问性当测试用例写（对比度、焦点顺序、键盘可达）；		业务价值句话：设计系统的成败不在组件数量，在"不合规的实现成本比合规的高"这个机制上。

- :focus-visible 解决什么问题？自定义控件（div 做的按钮）怎么补全交互语义？

		:focus-visible 把"键盘聚焦"从"所有聚焦"里分出来：鼠标点击不再显示焦点环（视觉噪音），Tab 键盘操作必须显示（可达性刚需），解决了老方案 :focus 两难的问题；		自定义控件三件套：role + tabindex（div 模拟按钮要 role=button tabindex=0）、键盘事件（Enter/Space 激活，方向键处理组合控件）、焦点可见（别把 outline: none 一删了之，用自定义焦点环，注意 offset 和圆角匹配）；		更高级的答案是直接反问"为什么要用 div 做按钮"——原生元素 + 样式重置（appearance:none）能白拿一半语义，自定义是语义不够时的补充不是默认。

- 响应式的现在时：容器查询、dvh、min()/clamp()、aspect-ratio 组合起来怎么用？

		思路从"屏幕尺寸"换到"容器和空间"：布局断点用容器查询（组件按自己拿到的宽度响应，和页面语境解耦，微前端/侧栏可拖场景刚需），全局排版用 clamp() 流式缩放（字号、间距不再跳变），尺寸单位用 100dvh 替代 100vh 修移动端地址栏跳动（dynamic viewport 随地址栏收起实时变化，small/large 用于"是否完全可见"的判断）；		aspect-ratio 防图片 CLS（预留比例再加载），min()/max() 替代一堆媒体查询；		答题落点：媒体查询管"页面级骨架"，容器查询管"组件级响应"，函数管"连续值"，三层各司其职才是现代写法。

- @property 和 CSS Houdini 给 CSS 带来什么？说一个 @property 的真实用法。

		@property 给自定义属性注册类型（syntax、initial-value、inherits），CSS 变量从"字符串"变成"有类型的值"——最大收益是可动画：未注册的变量过渡时只能整段跳变，注册成 <color>/<percentage> 后浏览器能做逐帧插值；渐变里的颜色变量动画就是典型场景；		副作用是作用域明确化：initial-value 让变量在注册时就生效（无初始值的注册只能用于平滑大写继承），减少"变量未定义时行为诡异"的排查；		Houdini 整体（Paint Worklet/Layout Worklet）态度可以坦率：规范有意思但浏览器支持收敛，Safari 对 worklet 一直冷淡，答到@property 这个落地深度就够了，别硬吹 Houdini。

- will-change 的作用是什么？为什么不能给所有动画元素都加上？（QQ音乐面经）

		它是一句提前声明：告诉浏览器这个元素马上要变，让它提前做层提升和独立合成，省掉动画开始那一刻才创建合成层造成的首帧卡顿；标准打法是配合 transform/opacity 这类合成器动画一起用；
		滥用有两层代价：每个提升层都要独立的纹理内存，移动端很容易内存吃紧、层爆炸反而掉帧；更隐蔽的是它改变渲染行为——will-change 会创建 containing block，fixed 定位的后代元素参照物跟着变，"加个属性弹窗位置漂移"这种诡异 bug 就是这么来的；
		正确姿势：动画开始前加、动画结束后去掉（或者 transitionend 里清理）；只对确认高频复现的动画元素常驻，别贴满全页；

## <a name='js'>JavaScript</a>


-  介绍js的基本数据类型。

		 Undefined、Null、Boolean、Number、String、
		 ECMAScript 2015 新增:Symbol(创建后独一无二且不可变的数据类型 )

-  介绍js有哪些内置对象？

		Object 是 JavaScript 中所有对象的父对象

		数据封装类对象：Object、Array、Boolean、Number 和 String
		其他对象：Function、Arguments、Math、Date、RegExp、Error

		参考：http://www.ibm.com/developerworks/cn/web/wa-objectsinjs-v1b/index.html

-  说几条写JavaScript的基本规范？

		1.不要在同一行声明多个变量。
		2.请使用 ===/!==来比较true/false或者数值
		3.使用对象字面量替代new Array这种形式
		4.不要使用全局函数。
		5.Switch语句必须带有default分支
		6.函数不应该有时候有返回值，有时候没有返回值。
		7.For循环必须使用大括号
		8.If语句必须使用大括号
		9.for-in循环中的变量 应该使用var关键字明确限定作用域，从而避免作用域污染。

-  JavaScript原型，原型链 ? 有什么特点？

		每个对象都会在其内部初始化一个属性，就是prototype(原型)，当我们访问一个对象的属性时，
		如果这个对象内部不存在这个属性，那么他就会去prototype里找这个属性，这个prototype又会有自己的prototype，
		于是就这样一直找下去，也就是我们平时所说的原型链的概念。
		关系：instance.constructor.prototype = instance.__proto__

		特点：
		JavaScript对象是通过引用来传递的，我们创建的每个新对象实体中并没有一份属于自己的原型副本。当我们修改原型时，与之相关的对象也会继承这一改变。


		 当我们需要一个属性的时，Javascript引擎会先看当前对象中是否有这个属性， 如果没有的话，
		 就会查找他的Prototype对象是否有这个属性，如此递推下去，一直检索到 Object 内建对象。
			function Func(){}
			Func.prototype.name = "Sean";
			Func.prototype.getInfo = function() {
			  return this.name;
			}
			var person = new Func();//现在可以参考var person = Object.create(oldObject);
			console.log(person.getInfo());//它拥有了Func的属性和方法
			//"Sean"
			console.log(Func.prototype);
			// Func { name="Sean", getInfo=function()}




-  JavaScript有几种类型的值？，你能画一下他们的内存图吗？

		栈：原始数据类型（Undefined，Null，Boolean，Number、String）
		堆：引用数据类型（对象、数组和函数）

		两种类型的区别是：存储位置不同；
		原始数据类型直接存储在栈(stack)中的简单数据段，占据空间小、大小固定，属于被频繁使用数据，所以放入栈中存储；
		引用数据类型存储在堆(heap)中的对象,占据空间大、大小不固定。如果存储在栈中，将会影响程序运行的性能；引用数据类型在栈中存储了指针，该指针指向堆中该实体的起始地址。当解释器寻找引用值时，会首先检索其在栈中的地址，取得地址后从堆中获得实体

	![Stated Clearly Image](http://www.w3school.com.cn/i/ct_js_value.gif)

- 如何将字符串转化为数字，例如'12.3b'?

		* parseFloat('12.3b');
		* 正则表达式，'12.3b'.match(/(\d)+(\.)?(\d)+/g)[0] * 1, 但是这个不太靠谱，提供一种思路而已。

- 如何将浮点数点左边的数每三位添加一个逗号，如12000000.11转化为『12,000,000.11』?

		function commafy(num){
			return num && num
				.toString()
				.replace(/(\d)(?=(\d{3})+\.)/g, function($1, $2){
					return $2 + ',';
				});
		}

- 如何实现数组的随机排序？
		
		方法一：
			var arr = [1,2,3,4,5,6,7,8,9,10];
			function randSort1(arr){
				for(var i = 0,len = arr.length;i < len; i++ ){
					var rand = parseInt(Math.random()*len);
					var temp = arr[rand];
					arr[rand] = arr[i];
					arr[i] = temp;
				}
				return arr;
			}
			console.log(randSort1(arr));
			
		方法二：
			var arr = [1,2,3,4,5,6,7,8,9,10];
			function randSort2(arr){
				var mixedArray = [];
				while(arr.length > 0){
					var randomIndex = parseInt(Math.random()*arr.length);
					mixedArray.push(arr[randomIndex]);
					arr.splice(randomIndex, 1);
				}
				return mixedArray;
			}
			console.log(randSort2(arr));

		方法三：
			var arr = [1,2,3,4,5,6,7,8,9,10];
			arr.sort(function(){
				return Math.random() - 0.5;
			})
			console.log(arr);

-  Javascript如何实现继承？

		1、构造继承
		2、原型继承
		3、实例继承
		4、拷贝继承

		原型prototype机制或apply和call方法去实现较简单，建议使用构造函数与原型混合方式。
		
			function Parent(){
				this.name = 'wang';
			}

			function Child(){
				this.age = 28;
			}
			Child.prototype = new Parent();//继承了Parent，通过原型

			var demo = new Child();
			alert(demo.age);
			alert(demo.name);//得到被继承的属性

- JavaScript继承的几种实现方式？
  - 参考：[构造函数的继承](http://www.ruanyifeng.com/blog/2010/05/object-oriented_javascript_inheritance.html)，[非构造函数的继承](http://www.ruanyifeng.com/blog/2010/05/object-oriented_javascript_inheritance_continued.html)；


-  javascript创建对象的几种方式？

		javascript创建对象简单的说,无非就是使用内置对象或各种自定义对象，当然还可以用JSON；但写法有很多种，也能混合使用。


		1、对象字面量的方式

			person={firstname:"Mark",lastname:"Yun",age:25,eyecolor:"black"};

		2、用function来模拟无参的构造函数

			function Person(){}
			var person=new Person();//定义一个function，如果使用new"实例化",该function可以看作是一个Class
			person.name="Mark";
			person.age="25";
			person.work=function(){
			alert(person.name+" hello...");
			}
			person.work();

		3、用function来模拟参构造函数来实现（用this关键字定义构造的上下文属性）

			function Pet(name,age,hobby){
			   this.name=name;//this作用域：当前对象
			   this.age=age;
			   this.hobby=hobby;
			   this.eat=function(){
			      alert("我叫"+this.name+",我喜欢"+this.hobby+",是个程序员");
			   }
			}
			var maidou =new Pet("麦兜",25,"coding");//实例化、创建对象
			maidou.eat();//调用eat方法


		4、用工厂方式来创建（内置对象）

			 var wcDog =new Object();
			 wcDog.name="旺财";
			 wcDog.age=3;
			 wcDog.work=function(){
			   alert("我是"+wcDog.name+",汪汪汪......");
			 }
			 wcDog.work();


		5、用原型方式来创建

			function Dog(){

			 }
			 Dog.prototype.name="旺财";
			 Dog.prototype.eat=function(){
			 alert(this.name+"是个吃货");
			 }
			 var wangcai =new Dog();
			 wangcai.eat();


		5、用混合方式来创建

			function Car(name,price){
			  this.name=name;
			  this.price=price;
			}
			 Car.prototype.sell=function(){
			   alert("我是"+this.name+"，我现在卖"+this.price+"万元");
			  }
			var camry =new Car("凯美瑞",27);
			camry.sell();

-  Javascript作用链域?

		全局函数无法查看局部函数的内部细节，但局部函数可以查看其上层的函数细节，直至全局细节。
		当需要从局部函数查找某一属性或方法时，如果当前作用域没有找到，就会上溯到上层作用域查找，
		直至全局函数，这种组织形式就是作用域链。

-  谈谈This对象的理解。

	```
  	this总是指向函数的直接调用者（而非间接调用者）；
	如果有new关键字，this指向new出来的那个对象；
	在事件中，this指向触发这个事件的对象，特殊的是，IE中的attachEvent中的this总是指向全局对象Window；
	```

-  eval是做什么的？

		它的功能是把对应的字符串解析成JS代码并运行；
		应该避免使用eval，不安全，非常耗性能（2次，一次解析成js语句，一次执行）。
		由JSON字符串转换为JSON对象的时候可以用eval，var obj =eval('('+ str +')');

-  什么是window对象? 什么是document对象?

		window对象是指浏览器打开的窗口。
		document对象是Documentd对象（HTML 文档对象）的一个只读引用，window对象的一个属性。

-  null，undefined 的区别？

		null 		表示一个对象是“没有值”的值，也就是值为“空”；
		undefined 	表示一个变量声明了没有初始化(赋值)；

		undefined不是一个有效的JSON，而null是；
		undefined的类型(typeof)是undefined；
		null的类型(typeof)是object；


		Javascript将未赋值的变量默认值设为undefined；
		Javascript从来不会将变量设为null。它是用来让程序员表明某个用var声明的变量时没有值的。

	    typeof undefined
			//"undefined"
			undefined :是一个表示"无"的原始值或者说表示"缺少值"，就是此处应该有一个值，但是还没有定义。当尝试读取时会返回 undefined；
			例如变量被声明了，但没有赋值时，就等于undefined

		typeof null
			//"object"
			null : 是一个对象(空对象, 没有任何属性和方法)；
			例如作为函数的参数，表示该函数的参数不是对象；

		注意：
			在验证null时，一定要使用　=== ，因为 == 无法分别 null 和　undefined
 			null == undefined // true
  			null === undefined // false

		再来一个例子：

			null
			Q：有张三这个人么？
			A：有！
			Q：张三有房子么？
			A：没有！

			undefined
			Q：有张三这个人么？
			A：有！
			Q: 张三有多少岁？
			A: 不知道（没有被告诉）

	参考阅读：[undefined与null的区别](http://www.ruanyifeng.com/blog/2014/03/undefined-vs-null.html)


-  写一个通用的事件侦听器函数。

			// event(事件)工具集，来源：github.com/markyun
			markyun.Event = {
				// 页面加载完成后
				readyEvent : function(fn) {
					if (fn==null) {
						fn=document;
					}
					var oldonload = window.onload;
					if (typeof window.onload != 'function') {
						window.onload = fn;
					} else {
						window.onload = function() {
							oldonload();
							fn();
						};
					}
				},
				// 视能力分别使用dom0||dom2||IE方式 来绑定事件
				// 参数： 操作的元素,事件名称 ,事件处理程序
				addEvent : function(element, type, handler) {
					if (element.addEventListener) {
						//事件类型、需要执行的函数、是否捕捉
						element.addEventListener(type, handler, false);
					} else if (element.attachEvent) {
						element.attachEvent('on' + type, function() {
							handler.call(element);
						});
					} else {
						element['on' + type] = handler;
					}
				},
				// 移除事件
				removeEvent : function(element, type, handler) {
					if (element.removeEventListener) {
						element.removeEventListener(type, handler, false);
					} else if (element.datachEvent) {
						element.detachEvent('on' + type, handler);
					} else {
						element['on' + type] = null;
					}
				},
				// 阻止事件 (主要是事件冒泡，因为IE不支持事件捕获)
				stopPropagation : function(ev) {
					if (ev.stopPropagation) {
						ev.stopPropagation();
					} else {
						ev.cancelBubble = true;
					}
				},
				// 取消事件的默认行为
				preventDefault : function(event) {
					if (event.preventDefault) {
						event.preventDefault();
					} else {
						event.returnValue = false;
					}
				},
				// 获取事件目标
				getTarget : function(event) {
					return event.target || event.srcElement;
				},
				// 获取event对象的引用，取到事件的所有信息，确保随时能使用event；
				getEvent : function(e) {
					var ev = e || window.event;
					if (!ev) {
						var c = this.getEvent.caller;
						while (c) {
							ev = c.arguments[0];
							if (ev && Event == ev.constructor) {
								break;
							}
							c = c.caller;
						}
					}
					return ev;
				}
			};

-  ["1", "2", "3"].map(parseInt) 答案是多少？

		parseInt() 函数能解析一个字符串，并返回一个整数，需要两个参数 (val, radix)，
		其中 radix 表示要解析的数字的基数。【该值介于 2 ~ 36 之间，并且字符串中的数字不能大于radix才能正确返回数字结果值】;
		但此处 map 传了 3 个 (element, index, array),我们重写parseInt函数测试一下是否符合上面的规则。

		function parseInt(str, radix) {
		    return str+'-'+radix;
		};
		var a=["1", "2", "3"];
		a.map(parseInt);  // ["1-0", "2-1", "3-2"] 不能大于radix

		因为二进制里面，没有数字3,导致出现超范围的radix赋值和不合法的进制解析，才会返回NaN
		所以["1", "2", "3"].map(parseInt) 答案也就是：[1, NaN, NaN]

		详细解析：http://blog.csdn.net/justjavac/article/details/19473199

-  事件是？IE与火狐的事件机制有什么区别？ 如何阻止冒泡？

		 1. 我们在网页中的某个操作（有的操作对应多个事件）。例如：当我们点击一个按钮就会产生一个事件。是可以被 JavaScript 侦测到的行为。
		 2. 事件处理机制：IE是事件冒泡、Firefox同时支持两种事件模型，也就是：捕获型事件和冒泡型事件；
		 3. ev.stopPropagation();（旧ie的方法 ev.cancelBubble = true;）


-  什么是闭包（closure），为什么要用它？

		闭包是指有权访问另一个函数作用域中变量的函数，创建闭包的最常见的方式就是在一个函数内创建另一个函数，通过另一个函数访问这个函数的局部变量,利用闭包可以突破作用链域，将函数内部的变量和方法传递到外部。

		闭包的特性：

		1.函数内再嵌套函数
		2.内部函数可以引用外层的参数和变量
		3.参数和变量不会被垃圾回收机制回收

		//li节点的onclick事件都能正确的弹出当前被点击的li索引
		 <ul id="testUL">
	        <li> index = 0</li>
	        <li> index = 1</li>
	        <li> index = 2</li>
	        <li> index = 3</li>
	    </ul>
		<script type="text/javascript">
		  	var nodes = document.getElementsByTagName("li");
			for(i = 0;i<nodes.length;i+= 1){
			    nodes[i].onclick = (function(i){
			              return function() {
			                 console.log(i);
			              } //不用闭包的话，值每次都是4
			            })(i);
			}
		</script>



		执行say667()后,say667()闭包内部变量会存在,而闭包内部函数的内部变量不会存在
		使得Javascript的垃圾回收机制GC不会收回say667()所占用的资源
		因为say667()的内部函数的执行需要依赖say667()中的变量
		这是对闭包作用的非常直白的描述

		  function say667() {
			// Local variable that ends up within closure
			var num = 666;
			var sayAlert = function() {
				alert(num);
			}
			num++;
			return sayAlert;
		}

		 var sayAlert = say667();
		 sayAlert()//执行结果应该弹出的667


-  javascript 代码中的"use strict";是什么意思 ? 使用它区别是什么？

		use strict是一种ECMAscript 5 添加的（严格）运行模式,这种模式使得 Javascript 在更严格的条件下运行,

		使JS编码更加规范化的模式,消除Javascript语法的一些不合理、不严谨之处，减少一些怪异行为。
		默认支持的糟糕特性都会被禁用，比如不能用with，也不能在意外的情况下给全局变量赋值;
		全局变量的显示声明,函数必须声明在顶层，不允许在非函数代码块内声明函数,arguments.callee也不允许使用；
		消除代码运行的一些不安全之处，保证代码运行的安全,限制函数中的arguments修改，严格模式下的eval函数的行为和非严格模式的也不相同;

		提高编译器效率，增加运行速度；
		为未来新版本的Javascript标准化做铺垫。


-  如何判断一个对象是否属于某个类？

 		  使用instanceof （待完善）
	       if(a instanceof Person){
	           alert('yes');
	       }

-  new操作符具体干了什么呢?

			 1、创建一个空对象，并且 this 变量引用该对象，同时还继承了该函数的原型。
	  	  	 2、属性和方法被加入到 this 引用的对象中。
	 		 3、新创建的对象由 this 所引用，并且最后隐式的返回 this 。

		var obj  = {};
		obj.__proto__ = Base.prototype;
		Base.call(obj);


-  用原生JavaScript的实现过什么功能吗？


-  Javascript中，有一个函数，执行时对象查找时，永远不会去查找原型，这个函数是？

		hasOwnProperty

		javaScript中hasOwnProperty函数方法是返回一个布尔值，指出一个对象是否具有指定名称的属性。此方法无法检查该对象的原型链中是否具有该属性；该属性必须是对象本身的一个成员。
		使用方法：
		object.hasOwnProperty(proName)
		其中参数object是必选项。一个对象的实例。
		proName是必选项。一个属性名称的字符串值。

		如果 object 具有指定名称的属性，那么JavaScript中hasOwnProperty函数方法返回 true，反之则返回 false。

-  JSON 的了解？

		JSON(JavaScript Object Notation) 是一种轻量级的数据交换格式。
		它是基于JavaScript的一个子集。数据格式简单, 易于读写, 占用带宽小
        如：{"age":"12", "name":"back"}

        JSON字符串转换为JSON对象:
		var obj =eval('('+ str +')');
		var obj = str.parseJSON();
		var obj = JSON.parse(str);

		JSON对象转换为JSON字符串：
		var last=obj.toJSONString();
		var last=JSON.stringify(obj);

-  `[].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})` 能解释一下这段代码的意思吗？


-  js延迟加载的方式有哪些？

		defer和async、动态创建DOM方式（用得最多）、按需异步载入js


-  Ajax 是什么? 如何创建一个Ajax？

		ajax的全称：Asynchronous Javascript And XML。
		异步传输+js+xml。
		所谓异步，在这里简单地解释就是：向服务器发送请求的时候，我们不必等待结果，而是可以同时做其他的事情，等到有了结果它自己会根据设定进行后续操作，与此同时，页面是不会发生整页刷新的，提高了用户体验。

		(1)创建XMLHttpRequest对象,也就是创建一个异步调用对象
		(2)创建一个新的HTTP请求,并指定该HTTP请求的方法、URL及验证信息
		(3)设置响应HTTP请求状态变化的函数
		(4)发送HTTP请求
		(5)获取异步调用返回的数据
		(6)使用JavaScript和DOM实现局部刷新

- Ajax 解决浏览器缓存问题？

		1、在ajax发送请求前加上 anyAjaxObj.setRequestHeader("If-Modified-Since","0")。

        2、在ajax发送请求前加上 anyAjaxObj.setRequestHeader("Cache-Control","no-cache")。

        3、在URL后面加上一个随机数： "fresh=" + Math.random();。

        4、在URL后面加上时间戳："nowtime=" + new Date().getTime();。

        5、如果是使用jQuery，直接这样就可以了 $.ajaxSetup({cache:false})。这样页面的所有ajax都会执行这条语句就是不需要保存缓存记录。

-  同步和异步的区别?

	同步的概念应该是来自于OS中关于同步的概念:不同进程为协同完成某项工作而在先后次序上调整(通过阻塞,唤醒等方式).同步强调的是顺序性.谁先谁后.异步则不存在这种顺序性.



	同步：浏览器访问服务器请求，用户看得到页面刷新，重新发请求,等请求完，页面刷新，新内容出现，用户看到新内容,进行下一步操作。

	异步：浏览器访问服务器请求，用户正常操作，浏览器后端进行请求。等请求完，页面不刷新，新内容也会出现，用户看到新内容。



	（待完善）

-  如何解决跨域问题?

		jsonp、 iframe、window.name、window.postMessage、服务器上设置代理页面

-  页面编码和被请求的资源编码如果不一致如何处理？

-  服务器代理转发时，该如何处理cookie？

		nginx
	

-  模块化开发怎么做？

	 [ 立即执行函数](http://benalman.com/news/2010/11/immediately-invoked-function-expression/),不暴露私有成员

		    var module1 = (function(){
		    　　　　var _count = 0;
		    　　　　var m1 = function(){
		    　　　　　　//...
		    　　　　};
		    　　　　var m2 = function(){
		    　　　　　　//...
		    　　　　};
		    　　　　return {
		    　　　　　　m1 : m1,
		    　　　　　　m2 : m2
		    　　　　};
		    　　})();

	（待完善）

-  谈一谈你对ECMAScript6的了解？

-  ECMAScript6 怎么写class么，为什么会出现class这种东西?

-  异步加载JS的方式有哪些？

	      (1) defer，只支持IE

	      (2) async：

	      (3) 创建script，插入到DOM中，加载完毕后callBack

- documen.write和 innerHTML的区别

		document.write只能重绘整个页面

		innerHTML可以重绘页面的一部分

- DOM操作——怎样添加、移除、移动、复制、创建和查找节点?

		（1）创建新节点
		  createDocumentFragment()    //创建一个DOM片段
		  createElement()   //创建一个具体的元素
		  createTextNode()   //创建一个文本节点
		（2）添加、移除、替换、插入
		  appendChild()
		  removeChild()
		  replaceChild()
		  insertBefore() //在已有的子节点前插入一个新的子节点
		（3）查找
		  getElementsByTagName()    //通过标签名称
		  getElementsByName()    //通过元素的Name属性的值(IE容错能力较强，会得到一个数组，其中包括id等于name值的)
		  getElementById()    //通过元素Id，唯一性

-  .call() 和 .apply() 的区别？


		  例子中用 add 来替换 sub，add.call(sub,3,1) == add(3,1) ，所以运行结果为：alert(4);

		  注意：js 中的函数其实是对象，函数名是对 Function 对象的引用。

			function add(a,b)
			{
			    alert(a+b);
			}

			function sub(a,b)
			{
			    alert(a-b);
			}

			add.call(sub,3,1);



-  数组和对象有哪些原生方法，列举一下？

-  JS 怎么实现一个类。怎么实例化这个类

-  JavaScript中的作用域与变量声明提升？

-  如何编写高性能的Javascript？

-  那些操作会造成内存泄漏？

-  需求：实现一个页面操作不会整页刷新的网站，并且能在浏览器前进、后退时正确响应。给出你的技术实现方案？

- 如何判断当前脚本运行在浏览器还是node环境中？（阿里）

		this === window ? 'browser' : 'node';

		通过判断Global对象是否为window，如果不为window，当前脚本没有运行在浏览器中

-  移动端最小触控区域是多大？

-  把 Script 标签 放在页面的最底部的body封闭之前 和封闭之后有什么区别？浏览器会如何解析它们？

-  移动端的点击事件的有延迟，时间是多久，为什么会有？ 怎么解决这个延时？（click 有 300ms 延迟,为了实现safari的双击事件的设计，浏览器要知道你是不是要双击操作。）

-  Node.js的适用场景？

-  (如果会用node)知道route, middleware, cluster, nodemon, pm2, server-side rendering么?

- 什么是“前端路由”?什么时候适合使用“前端路由”? “前端路由”有哪些优点和缺点?

- 知道什么是webkit么? 知道怎么用浏览器的各种工具来调试和debug代码么?

		Chrome,Safari浏览器内核。

- 如何测试前端代码么? 知道BDD, TDD, Unit Test么? 知道怎么测试你的前端工程么(mocha, sinon, jasmin, qUnit..)?

- 用js实现千位分隔符?(来源：[前端农民工](http://div.io/topic/744)，提示：正则+replace)


		参考：http://www.tuicool.com/articles/ArQZfui
		function commafy(num) {
		    return num && num
		        .toString()
		        .replace(/(\d)(?=(\d{3})+\.)/g, function($0, $1) {
		            return $1 + ",";
		        });
		}
		console.log(commafy(1234567.90)); //1,234,567.90



- What is a Polyfill?

		polyfill 是“在旧版浏览器上复制标准 API 的 JavaScript 补充”,可以动态地加载 JavaScript 代码或库，在不支持这些标准 API 的浏览器中模拟它们。
		例如，geolocation（地理位置）polyfill 可以在 navigator 对象上添加全局的 geolocation 对象，还能添加 getCurrentPosition 函数以及“坐标”回调对象，
		所有这些都是 W3C 地理位置 API 定义的对象和函数。因为 polyfill 模拟标准 API，所以能够以一种面向所有浏览器未来的方式针对这些 API 进行开发，
		一旦对这些 API 的支持变成绝对大多数，则可以方便地去掉 polyfill，无需做任何额外工作。

- 做的项目中，有没有用过或自己实现一些 polyfill 方案（兼容性处理方案）？

		比如： html5shiv、Geolocation、Placeholder

- 我们给一个dom同时绑定两个点击事件，一个用捕获，一个用冒泡。会执行几次事件，会先执行冒泡还是捕获？


- 使用JS实现获取文件扩展名？

		function getFileExtension(filename) {
		  return filename.slice((filename.lastIndexOf(".") - 1 >>> 0) + 2);
		}

		String.lastIndexOf() 方法返回指定值（本例中的'.'）在调用该方法的字符串中最后出现的位置，如果没找到则返回 -1。
		对于'filename'和'.hiddenfile'，lastIndexOf的返回值分别为0和-1无符号右移操作符(»>) 将-1转换为4294967295，将-2转换为4294967294，这个方法可以保证边缘情况时文件名不变。
		String.prototype.slice() 从上面计算的索引处提取文件的扩展名。如果索引比文件名的长度大，结果为""。

- Webpack热更新实现原理?

		1. Webpack编译期，为需要热更新的 entry 注入热更新代码(EventSource通信)
		2. 页面首次打开后，服务端与客户端通过 EventSource 建立通信渠道，把下一次的 hash 返回前端
		3. 客户端获取到hash，这个hash将作为下一次请求服务端 hot-update.js 和 hot-update.json的hash
		4. 修改页面代码后，Webpack 监听到文件修改后，开始编译，编译完成后，发送 build 消息给客户端
		5. 客户端获取到hash，成功后客户端构造hot-update.js script链接，然后插入主文档
		6. hot-update.js 插入成功后，执行hotAPI 的 createRecord 和 reload方法，获取到 Vue 组件的 render方法，重新 render 组件， 继而实现 UI 无刷新更新。

- 请介绍一下JS之事件节流？

- 什么是JS的函数防抖？

- 说说 Promise.all、allSettled、race、any 的区别？

		all：全成功才成功，一个失败立刻失败（但不会取消其余请求）；
		allSettled：等全部落定，返回 {status, value/reason} 数组，永不 reject，适合"每个请求都要有结果"的场景（批量上报、聚合接口降级）；
		race：第一个完成的定胜负，不分成败，常配超时（新起一个 setTimeout reject 去 race）；
		any：第一个成功的算赢，全失败才抛 AggregateError，多源/多 CDN 容灾场景。
		追问点：Promise.all 失败为什么不会取消其他 promise，怎么配合 AbortController 做真取消。

- async/await 的错误处理怎么写更优雅？每段都 try/catch 还是统一封装，你怎么选？

		原则：别满屏 try/catch，也别裸奔。业务错误往上冒泡，边界处统一收（请求拦截器、事件入口、React ErrorBoundary）；
		常用封装是 Go 风格：const [err, data] = await to(promise)（把 promise 包一层 catch 返回数组）；确需降级的地方才单独 try/catch；
		顺带高频追问：for...of 里的 await 是串行，要并发用 Promise.all(settled) + map，这比背错误处理格式更能看出水平。

- 事件循环：给一段代码说输出顺序（宏任务/微任务综合变体题，现在基本都是这种考法）。

		执行模型：一轮宏任务 -> 清空所有微任务 -> （需要时）渲染下一帧；
		易错点集中在：await 后面的代码等价于then回调属于微任务、微任务里再产生的微任务插队顺序、setTimeout(fn,0) 与 Promise.resolve().then 的先后、async 函数 immediate 执行到第一个 await 前是同步的；
		Node 环境还会追加 process.nextTick / setImmediate /微任务与timers的阶段关系，说答案前先问清是浏览器还是 Node。
		这题没捷径，拿真题手推几遍就稳了。

- Proxy 和 Reflect 的应用场景？Vue3 响应式为什么从 defineProperty 换成 Proxy？

		defineProperty 只能拦截对象上"已存在的单个属性"；Proxy 是整个对象的拦截层（get/set/has/deleteProperty 等13种陷阱）；
		Vue3 换 Proxy 的直接收益：新增/删除属性可感知（不再需要 Vue.set）、数组索引和 length 变化可感知、可以懒代理（访问到嵌套对象才包一层，大对象初始化开销小）；
		Reflect 用来保证默认行为正确（和 Proxy 的 trap 一一对应，负责把 receiver 传下去）；
		代价是 Proxy 无法 polyfill，这就是 Vue3 放弃 IE11 的直接原因。

- WeakMap 和 Map 的区别？举一个 WeakMap 的真实使用场景？

		WeakMap 的 key 只能是对象、不阻塞垃圾回收、不可遍历（随时可能被回收，所以没法遍历）；
		真实场景：给对象/DOM 节点挂不泄漏的元数据（事件监听计数）、私有属性模拟、依赖收集的 targetMap、raw->proxy 缓存（Vue3 里就是 WeakMap）；
		一句话：以对象为 key 又不想引起内存泄漏，就用它。

- structuredClone() 和 JSON.parse(JSON.stringify()) 深拷贝的区别？

		JSON 法的问题：函数/symbol/undefined 丢失、Date 变字符串、RegExp/Map/Set 变空对象、NaN/Infinity 变 null、循环引用直接抛错；
		structuredClone 走结构化克隆算法：Date/RegExp/Map/Set/ArrayBuffer/循环引用都支持；但函数和 symbol 会抛错、DOM 节点不行；
		浏览器和 Node 17+ 都可用。面试建议手写版也要会（WeakMap 记录循环引用那版）。

- for...of、for...in、forEach 的区别？Iterator 遍历协议是怎样的？

		for...in 遍历可枚举的"键"（含原型链，数组别用，下标还是字符串）；
		for...of 走 Symbol.iterator 遍历"值"，数组/Map/Set/字符串/NodeList/生成器都行，可以 break；
		forEach 不能中断、也不会等待 async 回调；
		Iterator 协议：对象有 [Symbol.iterator]() 方法，返回带 next() 的迭代器，next() 产出 {value, done}；for...of、展开运算符、解构底层全是它。
		新增分：Iterator Helpers（.map/.filter 链式且惰性）Chrome 122+ / Node 22 已支持。

- Top-level await 的适用场景和坑？

		ESM 里不用包 async function 就能 await，适合初始化配置（读环境、预热连接）、动态 import 开关；
		坑：（1）模块求值被 await 阻塞，依赖它的整条 import 链都得等，可能拖慢启动；（2）只能在 ESM 用；（3）失败处理变复杂——模块级抛错会让整个依赖链挂掉；
		结论：应用入口/脚本随便用，公共库谨慎用。

- requestAnimationFrame 和 requestIdleCallback 的区别？长任务怎么拆分避免掉帧？

		rAF 每帧渲染前执行，动画和逐帧计算用它；rIC 在空闲时段执行，埋点上报、大列表预处理这类不急的活用它（Safari 支持较晚，要带 setTimeout 降级）；
		防掉帧的核心：把长任务切成不超过一帧预算的小块，用 rAF / scheduler.yield() 分片，跟 React Fiber 的时间切片是一个思想；
		这题经常和 Fiber、长列表优化串在一起问。

- 前端内存泄漏现在怎么排查？Chrome DevTools Memory 堆快照用过吗？

		常见来源：未清理的定时器、没解绑的监听（尤其 window/scroll/resize）、闭包持有大对象、三方实例没 dispose（地图/图表重灾区）、console 里挂着对象、detached DOM；
		手法：Memory 面板 Heap Snapshot 对比（操作前拍一次、操作后再拍，看 Detached DOM 和哪类对象持续增长），配合 Allocation timeline 看分配时机；
		React 里 "Can't perform a React state update on an unmounted component" 就是一个明确信号，useEffect 记得写返回清理函数。

- 手写题：防抖、节流、深拷贝、Promise 并发控制、数组扁平化、LRU、柯里化，现在面试怎么考？（更多是结合真实场景，不是干背）

		趋势是从"纯手写"变成"场景里夹手写"：搜索联想输入你怎么防抖？批量拉接口怎么做并发限制？虚拟列表配合什么缓存？
		考最多的：Promise 并发控制（限流器，配合真实批量场景）、LRU（Map 的插入顺序 + get/set）、节流（rAF 版比 setInterval 版更受青睐）、深拷贝（和 structuredClone 对比着讲）、扁平化（flat/Infinity 和手写栈/迭代两版都要会说）；
		防抖节流很少单独考了，但 timer、立即执行/延迟执行的细节一定要说得出。

- 事件循环：setTimeout / requestAnimationFrame / queueMicrotask / MessageChannel / requestIdleCallback 的触发时机和优先级，怎么排？

		一层层排：脚本和事件回调跑完 -> 清空微任务队列（Promise 回调、queueMicrotask）-> 渲染里程碑：rAF 在绘制前执行（样式计算前，动画的正确挂点）-> 一帧结束，空闲时段（默认 50ms 预算内）喂 requestIdleCallback，超时则降级为 setTimeout；MessageChannel 的 onmessage 是宏任务，排在新 task 里——React 调度器用它做让出后续接就是靠这个（见框架章节）；		高频考点：setTimeout(fn,0) 在渲染忙时会延到下一帧后，rAF 保证每帧一次且绘制前——动画用 rAF 不用定时器；微任务里不要再排微任务，会把渲染饿死；		能画出"宏任务->微任务->rAF->绘制->idle"这个环形图，这题就赢了。

- 设计模式在前端还剩多少价值？说说发布订阅、观察者、策略、代理在现代代码里的真实位置。

		剩下的是"命名能力"而不是"背诵 UML"：事件系统/状态管理订阅 = 发布订阅（解耦生产者消费者，代价是数据流变隐式，Redux 用单向流收编它）；Vue 响应式 = 代理模式（Proxy 拦截读写收集依赖，这比老的 defineProperty 观察者先进在能拦截新增删除和数组）；		策略模式活在日常每一行：按类型 map 查处理函数替代 switch（顺带解决分支不可 tree-shake）；装饰器/中间件链（koa、React HOC）是责任链+装饰器的混合；		我的态度：模式是重构之后的命名，不是编码之前的套用——面试时先讲场景再点名模式，顺序反了就是背书。

- 海量数据的展示和处理：虚拟列表之外还有哪些手段？Web Worker + OffscreenCanvas 能组合出什么？

		渲染层：虚拟列表是基础答案（只渲染视口 ± buffer，动态高度用估计+回收校正或 ResizeObserver）；再往上是 Canvas 自绘（万级节点，ECharts/D3 canvas 渲染器）、CSS content-visibility: auto（浏览器帮你跳过屏幕外渲染，成本低收益大）、分帧渲染（把循环切片塞进多个 rAF）；		数据层：解析和聚合丢给 Worker（大 JSON.parse、分组统计），主线程只收结果；图像/图表类输出可以 Worker 里直接画 OffscreenCanvas，连"传像素回主线程"这一步都省了；		交互层：增量视图（只维护排序/过滤后的索引数组）、二分定位视口区间、滚动节流用 rAF 对齐帧；		这题听的是分层意识：渲染、数据、交互三层的瓶颈和手段不一样。

- WebSocket 之外，实时 Web 还有哪些选型？SSE、WebTransport、Long polling 现在各自的位置。

		按需求形状选：服务端单向推送（通知、行情、AI 流式输出）SSE 最省事（HTTP 语义、自动重连、网关友好）；双向低延迟（协作、游戏、音视频信令）WebSocket；WebTransport 是新选项——基于 HTTP/3 QUIC，解决 WS 的头阻塞（每条流独立，丢包不殃及兄弟流）、支持 unordered/部分可靠，适合"流多且每条要独立"的场景（帧同步、大文件分块）；		Long polling 基本退役，但它的降级价值还在：企业内网/苛刻代理环境把 WS 掐死时，SSE/polling 是兜底；		坑位必答：WS 没有浏览器原生重连（要自己心跳 + 指数退避）、移动端切后台必然断线（产品层要处理"重连后状态补偿"）、SSE 的 HTTP/1 并发 6 条限制（HTTP/2 解决）。

- performance.mark / measure 和 User Timing API 怎么接入业务监控？和 PerformanceObserver 什么关系？

		mark/measure 是给"业务自定义指标"用的：请求发起/响应解析/状态更新/DOM 就绪各打一个 mark，measure 串成"搜索耗时=提交->列表渲染完成"这种有业务含义的分解，采集进 reportValue 上报，指标才能下钻（只报一个总耗时排查不了问题）；		PerformanceObserver 是统一的异步入口：buffered:true 可以拿到历史条目，按 entryTypes 订阅（largest-contentful-paint、event、long-animation-frame）——CWV 和 INP 的采集必须走它，别再手写监听；		加分项：LoAF（Long Animation Frames，Chrome 123+）替代老 longtask 能定位"这一帧里具体哪个脚本、哪次回调贡献了多少 ms"，排查 INP 的实战价值极高；75 分位上报、区分 mP/实时见 CWV 相关题目。

- WeakMap / WeakSet / FinalizationRegistry 的真实用途是什么？内存调试怎么做？

		Weak 系列的核心价值是"不阻止 GC + 以对象为键"：给 DOM 节点/实例挂私有元数据（缓存、权限标记）而对象销毁后自动走人，经典应用是代理缓存（target->proxy 映射）、按对象索引的私有字段（# 语法的底层就是 WeakMap）；		FinalizationRegistry 是对象被回收时的回调，听起来适合"清理"，但时机不保证、不保证执行，只能做非关键的资源提示，别拿它替代手动 dispose；		内存调试实操：DevTools Memory 的 heap snapshot 对比（三次快照法找泄漏链）、Allocation instrumentation on timeline 看增长曲线、Detached DOM 节点（console 里留着引用、监听器没解绑）是前端泄漏的头号形态——虚拟列表和事件总线是重灾区。

- __proto__ 是 ES 规范定义的吗？规范获取原型应该用什么？（米哈游面经）

		__proto__ 不属于 ES 主规范，它住在 Annex B（历史遗留附加章）里，是浏览器环境的既成事实；规范路径是 Object.getPrototypeOf() / Object.setPrototypeOf()，创建对象时传原型用 Object.create(proto)；
		这题面试官实际在等两件事：一是你分得清"语言规范"和"实现惯例"这两个概念；二是顺手讲清 prototype 和 __proto__ 的关系——函数对象的 prototype 属性，就是它的实例的 [[Prototype]] 内部槽位，__proto__ 只是访问这个槽位的一个历史 getter/setter；
		带一个性能冷知识：高频读写 __proto__ 会让 V8 的隐藏类（Shapes）失效、内联缓存崩掉，这也是运行时不该用 setPrototypeOf 改对象形状的原因——类型要在一开始定好，引擎才能给它画出稳定形状；

- 为什么基础类型在栈、对象在堆？堆和栈的分工到底是什么？（米哈游面经）

		栈管"大小确定、生命周期跟执行帧走"的东西：原始值和对象的引用存栈，分配回收就是移动栈指针，几乎零成本；堆管"大小不定、可能被长期持有"的对象实体，靠 GC 回收；
		所以准确说法不是"值在栈、对象在堆"，而是"引用在栈、实体在堆"——变量指向堆里的对象；另一个易错点是闭包：被闭包捕获的局部变量会被引擎搬进堆上的上下文对象，不随函数返回销毁，讲闭包内存不带上这层就是背了一半；
		继续往下是 V8 的分代：小对象进新生代（Semi-space 复制，存活对象少时复制成本极低），活久了晋升老生代（标记-整理）；这解释了为什么"大量短命小对象"的 GC 压力反而小，也是前端别在热路径疯狂造临时对象之外、真正该关注的是长生命周期引用链的原因；

- eval 和 new Function 的区别？你会优先选哪个？（Shopee面经）

		核心差异是作用域：eval 在当前作用域里执行字符串，能读写局部变量，还会让整个函数放弃大量编译优化；new Function 造出的函数只能看到全局作用域加自己的参数，局部变量对它不可见，对当前作用域无污染；
		二选一我选 new Function：影响面可控、不破坏外层函数的优化；低代码的表达式求值、动态加载配置这类场景，老写法就是它；
		但答案必须把安全说完：两者本质都是"把字符串当代码执行"，用户输入能进来就是注入级风险；正经工程做法是受限表达式引擎（解析成白名单 AST 再求值，比如 expr-eval 这类思路），而不是在两个危险选项里挑一个温和点的；

- Promise 构造器里同步 throw，后面的 .catch 能捕获得到吗？（Shopee面经）

		能。executor 同步 throw 会被 Promise 内部捕获，状态直接置为 rejected，后面的 .catch 在微任务里正常收到；但如果 throw 之前已经调用过 resolve，状态不可逆，catch 拿到的是先 resolve 的值——状态机的"先到先得"优先级高于一切；
		这题真正考的是 Promise 状态机三规则：状态只能从 pending 单向变更、一次变更永久生效、executor 同步执行而 then 回调永远是微任务；把三条说全，再杂的输出题都能推；
		补一个 ES2024 的新东西显出现代：Promise.withResolvers() 把 resolve/reject 取到外部持有，封装"发请求等回包"这类异步边界时，不用再用"构造器里挖洞抓引用"的老写法；

- 手写：实现一个第一次挂载不执行的 useEffect？（拼多多面经）

		思路是一个 useRef 开关：function useUpdateEffect(effect, deps) { const mounted = useRef(false); useEffect(() => { if (!mounted.current) { mounted.current = true; return; } return effect(); }, deps); } 首次运行只翻标记不执行，之后照常；
		依赖比较完全交给原生 useEffect，不要在自造 hook 里重新实现一套依赖数组逻辑——那是最容易出 bug 的过度工程；
		追问点必然是"为什么用 ref 不用 state"：这个标记不需要也不应该触发渲染，用 state 白白多一次 render 还引入异步时序问题；再用一句话收尾场景：首帧不想重复拉取、不想打重复埋点的组件，用它替换"自己造 mount 标记"的土办法；

- 给一个 json 描述的虚拟 DOM 对象，怎么实现一个把它还原成真实 DOM 的函数？（拼多多面经）

		递归 + createElement：function render(vnode) { const el = document.createElement(vnode.tag); for (const [k, v] of Object.entries(vnode.props || {})) { k.startsWith('on') ? el.addEventListener(k.slice(2).toLowerCase(), v) : el.setAttribute(k, v); } (vnode.children || []).forEach(c => el.appendChild(typeof c === 'string' ? document.createTextNode(c) : render(c))); return el; }
		手写的区分度在细节：文本节点要判 typeof、事件名 on 前缀的映射、children 里嵌套数组要不要拍平、危险属性（内联事件、javascript: 协议）怎么过滤——过滤这步能自然过渡到 XSS 防御和 dangerouslySetInnerHTML 的边界；
		这题是从 React 虚拟 DOM 倒推出来的"它到底在干嘛"：能亲手把 vnode 变成真 DOM，再去看 diff 就是在两棵树递归比对的图景，理解完全不一样；

- 依赖注入（DI）和 IoC 在前端有哪些真实应用？哪些开源项目在用？（QQ音乐/蔚来面经）

		先讲大白话：IoC 是"我不再自己 new 依赖，创建和使用分离"，DI 是最常见的落地——依赖从构造函数/参数注入进来；前端重一点的实现是 Angular/NestJS 的装饰器 DI 和 InversifyJS 容器，轻量的就是 React Context、Vue 的 provide/inject，本质都是运行时注入；
		最大收益是可替换性：单测注入 mock 实现、按环境换存储/网关/埋点实现，业务代码不动；代价是间接层的调试成本和心智负担，中小项目硬套容器就是过度设计，这个边界判断比会不会用更重要；
		"开源框架里哪见过"的标准答案：webpack 执行 loader/plugin 时把 compiler 注入给你、Vite 插件共享 vite 实例、Express 中间件链注入 req/res——都是"能力由外部传入"的变体；能报出具体框架里名字，这题就赢了；

#### <a name='other'>ECMAScript6 相关</a>

- Object.is() 与原来的比较操作符“ ===”、“ ==”的区别？

		两等号判等，会在比较时进行类型转换；
		三等号判等(判断严格)，比较时不进行隐式类型转换,（类型不同则会返回false）；

		Object.is 在三等号判等的基础上特别处理了 NaN 、-0 和 +0 ，保证 -0 和 +0 不再相同，
		但 Object.is(NaN, NaN) 会返回 true.

 		Object.is 应被认为有其特殊的用途，而不能用它认为它比其它的相等对比更宽松或严格。

- ES6是如何实现编译成ES5的？

- css-loader的原理？


#### <a name='ts'>TypeScript 相关</a>

- type 和 interface 的区别？什么场景必须用其中一个？

		日常九成场景可以互换。真正的差异点：interface 支持声明合并（同名自动合并，给第三方库和全局 Window 补类型靠它），能被 class implements；
		type 能写联合/交叉/条件/映射类型、能给元组和函数签名起名；
		性能上 interface 的编译期关系检查更友好，复杂递归 type 容易报 "excessively deep"；
		团队里统一约定比选哪个更重要。

- unknown 和 any 的区别？为什么说 any 是类型系统的漏洞？（字节）

		any 等于关闭检查（双向兼容一切），unknown 是"有值但不知道类型"，用之前必须收窄（typeof / in / 判别字段）；
		所有进入 TS 的外部数据（接口返回、JSON.parse、postMessage）理想类型都是 unknown，编译器会逼你校验；
		这题面试官其实想听你对类型边界的理解：开 strict / noImplicitAny 后收益在哪、什么时候才允许 as。

- 泛型约束（extends）、条件类型、infer 关键字，举一个实际例子？

		约束：function pick<T, K extends keyof T>(obj: T, keys: K[]): Pick<T, K>；
		条件类型 + infer 最经典的例子就是 ReturnType：type MyReturnType<T> = T extends (...args: any[]) => infer R ? R : never；
		再比如取数组元素类型：T extends (infer U)[] ? U : never；
		infer 会在解构式位置"占位推断"，会用它基本算摸到了类型体操的门口。

- 联合类型、交叉类型、可辨识联合（discriminated union）怎么用？

		联合是"或"（A | B），交叉是"且"（A & B 同时满足）；
		可辨识联合：每个成员带一个字面量标签字段，switch (action.type) 自动收窄——Redux action、接口多态返回（{status:'ok',data} | {status:'err',code}）都靠它；
		配套的穷尽检查：default 分支赋给 never，以后新增成员编译器会提醒你漏处理。

- satisfies 操作符和 as 断言的区别？（TS 4.9+）

		as 是断言（"别检查，听我的"），会把错误盖住；satisfies 是"检查形状，但保留推断"：
		const palette = { bg: '#fff' } satisfies Record<string, `#${string}`>，既校验了所有值，palette.bg 还保留字面量类型（as 之后只剩 Record 视角）；
		配置对象 + 想要精确类型时最有用，现在是推荐写法，替代大部分 as 的场景。

- 手写工具类型：Partial、Pick、Omit、ReturnType，实现过哪几个？

		都是映射类型一行事，能手写说明理解了 in / keyof / 修饰符：
		type MyPartial<T> = { [K in keyof T]?: T[K] }；
		type MyPick<T, K extends keyof T> = { [K in K]: T[K] }；
		type MyOmit<T, K extends PropertyKey> = Pick<T, Exclude<keyof T, K>>；
		追问一般落在 Exclude / Extract 和 distributes 条件类型对 union 的分配律上。

- tsconfig 里 strict、moduleResolution、skipLibCheck、isolatedModules 都是干什么的？

		strict 是一组开关的总闸（noImplicitAny、strictNullChecks 等，strictNullChecks 是甜苦分水岭）；
		moduleResolution 决定 import 路径如何解析（classic / node / bundler / node16），配 module 版本要配套，Vite 项目用 bundler；
		skipLibCheck 跳过三方 .d.ts 的类型检查，提速明显；
		isolatedModules 按"单文件转译"的约束来（esbuild/swc 都要求它），禁 re-export 类型、禁非const enum 等；构建工具换了之后一堆 tsconfig 报错的根源都在这几行。

- as const 和 enum，项目里你怎么用？为什么说 enum 现在不太被推荐？

		as const 把字面量整体锁死为只读字面量类型，配置表、路由元信息都能拿到最精确推断，配合 (typeof x)[keyof typeof x] 还能生成 union；
		enum 的问题：编译出运行时 IIFE（包体积和 tree-shaking 不友好）、数字枚举可以反向映射容易埋坑、const enum 在 isolatedModules（esbuild/swc）下被禁；
		现在主流做法：union of string literals + as const 对象替代 enum；TS 5.0 的 satisfies 和 later 的 enum 演进（TS 7 原生 go 编译器）都说明官方也在收口这块。

- declare、namespace、declare module 这些"全局声明"语法现在还有用武之地吗？

		有，但场景收敛：给无类型的第三方脚本（老 jQuery 插件、埋点 SDK、window.__CONFIG__）写环境声明，declare global 补 window 属性；declare module 'xxx' 做模块补类型或通配符兜底（图片/CSS 导入）；namespace 新项目别用（它和 ES module 是两套时代），但读老代码和 @types 里的历史包袱要认识；		更现代的做法：优先找社区 @types，没有就在项目里写窄声明（只声明用到的部分，别全量翻译），.d.ts 进版本控制；		这题本质考"你对类型系统的边界理解"：类型是运行时外层的说明书，说明书可以分层写，但别拿说明书当运行时（declare 不产生任何代码）。

- 怎么做"没有 any 的 lint 策略"？no-explicit-any 落地时怎么处理第三方库和渐进迁移？

		先分层：新代码 strict + no-any 硬拦，存量按文件/目录豁免逐步收紧（oxlint/biome 支持按规则分级）；逃生舱要留但要可审计：unknown + 显式收窄是正路，实在要用 any 就带 eslint-disable 注释 + 原因，数量当技术债指标追踪；		第三方库无类型：优先 @types，缺失就自己 patch 一个最小 .d.ts（只声明用到的 API），比 any 断言可控；动态边界（JSON、postMessage、DOM querySelector）必须经 schema 验证（zod）再进类型系统——这是"verify don't type"的核心；		高年级答案：any 的问题不是"不精确"，是它会传染（any 参与运算结果还是 any），一放开整个表达式的检查就全没了，所以宁可用 unknown 逼自己收窄。

- 类型体操在实际业务里到底用在哪？能举两三个真实场景吗？

		场景一：API 层的端到端类型——OpenAPI/GraphQL schema 生成类型 + 泛型请求封装，接口一改类型跟着变，联调错误编译期就爆（Orval/Codegen 路线，比手写 interface 稳一个量级）；		场景二：组件库/工具库的公共 API——多态组件的 as prop + JSX.IntrinsicElements 映射、表单库的字段路径推导（get('user.address.city') 拼错编译报错）、状态库的 action 类型推断，这些库的内部复杂换调用方的简单，值得有人写重型类型；		场景三：业务状态机——判别联合 + exhaustiveness check（default 分支 never 检查），状态加了一枚编译器逼你处理所有分支，这类需求用工具类型 + satisfies 就够；		我的红线：业务页面里炫 infer 套五层就是负资产，可读性优先——面试能说出"什么时候不用"比会写更值钱。

- satisfies 到底解决了什么问题？和 as 的区别是什么？为什么需要两个关键字？

		satisfies 是 4.9 补的缺口：让表达式按目标类型检查但不改变推断结果。as 是单向断言（宽到窄强转，过了检查但骗了下游，拼错的属性名照样放行）；类型标注（const x: T）会截断推断（拿到字面量类型就丢了）；		典型例子：const palette = { red: [255,0,0], green: '#00ff00' } satisfies Record<string, string|number[]>——检查每项合法，同时 palette.green 仍是 string（能调 .toUpperCase）、还能发现漏了 blue 之外的拼写错误；as 版本丢成员类型，标注版本丢字面量精度；		一句话总结：satisfies 是"带检查的保持推断"，as 是"放弃检查的改类型"——日常默认 satisfies 和标注，as 只留给真正的断言（运行时已验证过）。

- 配置 tsconfig 时，skipLibCheck、forceConsistentCasingInFileNames、isolatedModules、verbatimModuleSyntax 分别防什么问题？

		skipLibCheck 跳过 .d.ts 内部检查，换编译速度（默认开，代价是三方类型冲突漏检）；forceConsistentCasingInFileNames 防大小写引入（mac 不区分、Linux 构建炸，跨平台必开）；		isolatedModules 是给"单文件转译器"（esbuild/swc/babel）立规矩：禁止跨文件 re-export 类型这种需要全量语义的操作，让"编译快"和"语义正确"不打架；verbatimModuleSyntax 更进一步：import type 必须显式写，写了就保留——解决"类型导入被转译器误删/运行时导入被误删"的双向事故，也是 ESM/CJS 混用的显式化；		这题答出"为什么现代工具链要求显式 type 导入"（转译器只看单文件，分不清你是类型还是值）就到位了。

## <a name='other'>前端框架</a>

- React 使用场景？

			逻辑复杂单页应用，偏中后台管理系统，纯展示性的UI页面不合适、

- 描述一下React 生命周期

			渲染过程调用到的生命周期函数，主要几个要知道；
			* constructor 
			* getInitialState 
			* getDefaultProps 
			* componentWillMount 
			* render 
			* componentDidMount 

			更新过程

			* componentWillReceiveProps 
			* shouldComponentUpdate 
			* componentWillUpdate 
			* render 
			* componentDidUpdate 

			卸载过程

			componentWillUnmount

		（2026 注：以上是老版 class 生命周期。React 16.3 后 Will 系被废弃/改名，新增 getDerivedStateFromProps、getSnapshotBeforeUpdate；17+ 已移除旧 API；函数组件 + Hooks 时代，能讲清楚"并发渲染下旧生命周期为什么不安全"才是考点。）


- 实现组件有哪些方式？

		React.createClass 使用API来定义组件
		React ES6 class component 用 ES6 的class 来定义组件
		Functional stateless component 通过函数定义无状态组件

		（2026 注：createClass 移除多年；函数组件 + Hooks 是默认写法，class 只剩存量维护；React Compiler 出现后"函数组件要不要 memo"这个老问题也在变。）


- 应该在React生命周期的什么阶段发出ajax请求，为什么？

				AJAX请求应在 componentDidMount函数 进行请求。

- shouldComponentUpdate函数有什么作用？

				shouldComponentUpdate是一个允许我们自行决定某些组件（以及他们的子组件）是否进行更新的生命周期函数，reconciliation的最终目的是尽可能以最有效的方式去根据新的state更新UI，
				如果你已经知道UI的哪些状态无需进行改变，就没必要去让React去判断它是否该改变。 让shouldComponentUpdate返回falss, React就会让当前的组件和其子组件保持不变。

- 当组件的setState函数被调用之后，发生了什么？

				React会做的第一件事就是把你传递给setState的参数对象合并到组件原先的state。这个事件会导致一个“reconciliation”（调和）的过程。reconciliation的最终目标就是，
				尽可能以最高效的方法，去基于新的state来更新UI。为了达到这个目的，React会构建一个React元素树（你可以把这个想象成一个表示UI的一个对象）。一旦这个树构建完毕，
				React为了根据新的state去决定UI要怎么进行改变，它会找出这棵新树和旧树的不同之处。React能够相对精确地找出哪些位置发生了改变以及如何发生了什么变化，
				并且知道如何只通过必要的更新来最小化重渲染。

- 为什么循环产生的组件中要利用上key这个特殊的prop？

				Keys负责帮助React跟踪列表中哪些元素被改变/添加/移除。React利用子元素的key在比较两棵树的时候，快速得知一个元素是新的还是刚刚被移除。没有keys，React也就不知道当前哪一个的item被移除了。

- React-router 路由的实现原理？

- 说说React Native,Weex框架的实现原理？

- 受控组件(Controlled Component)与非受控组件(Uncontrolled Component)的区别

- refs 是什么?

			Refs是能访问DOM元素或组件实例的一个函数；

- React为什么自己定义一套事件体系呢，与浏览器原生事件体系有什么关系？

- 什么时候应该选择用class实现一个组件，什么时候用一个函数实现一个组件？

			组件用到了state或者用了生命周期函数，那么就该使用Class component。其他情况下，应使用Functional component。

- 什么是HoC（Higher-Order Component）？适用于什么场景？

			高阶组件就是一个 React 组件包裹着另外一个 React 组件

- 并不是父子关系的组件，如何实现相互的数据通信？

			使用父组件，通过props将变量传入子组件 （如通过refs，父组件获取一个子组件的方法，简单包装后，将包装后的方法通过props传入另一个子组件 ）

- 用过 React 技术栈中哪些数据流管理库？

			Redux\Dva

- Redux是如何做到可预测呢？

- Redux将React组件划分为哪两种？

- Redux是如何将state注入到React组件上的？

- 请描述一次完整的 Redux 数据流

- React的批量更新机制 BatchUpdates？

- React与Vue，各自的组件更新进行对比，它们有哪些区别？

- React 16/17 之后废弃了哪些生命周期？为什么？新的生命周期有哪些？

		被废弃/改名的：componentWillMount、componentWillReceiveProps、componentWillUpdate（三个 Will 系在并发渲染下可能被中断后重新执行，副作用会翻倍）；
		新的：getDerivedStateFromProps（静态，明确"由 props 派生 state"）、getSnapshotBeforeUpdate + componentDidUpdate（更新前抓快照）；
		函数组件时代这些基本被 useEffect / useMemo 吸收了。能把"为什么并发渲染下旧 API 不安全"讲清楚，比背名字值钱得多。

- React Hooks 为什么不能写在条件语句里？（调用顺序、链表实现）（字节）

		Hooks 的状态存在 fiber 上的一条链表里，靠"调用顺序"一一对应；条件/循环会让这次渲染的第 N 个 hook 对不上上次的槽位，状态直接错位；
		所以 React 在 dev 下校验 hook 数量并报错；
		延伸追问：为什么自定义 Hook 里可以用条件（顺序规则只约束最外层调用序列）。

- useEffect 和 useLayoutEffect 的区别？什么场景必须用后者？

		useLayoutEffect 在 DOM 变更后、浏览器绘制前同步执行，会阻塞绘制；useEffect 在绘制后异步执行；
		必须用 layout 的场景：先读布局再同步改、否则用户会看到跳变的（tooltip 定位、滚动位置恢复、受控元素高度）；
		其他一律用 effect。注意 SSR 下 useLayoutEffect 会告警（Next 里的常见坑）。

- React 的 Fiber 架构解决了什么问题？时间切片是怎么回事？

		老的栈式协调不可中断，大树的 diff 一口气跑完会卡死主线程，动画和输入掉帧；
		Fiber 把每个组件变成一个可暂停/恢复/放弃的工作单元（child/sibling/return 三指针链表），workLoop 在一个 5ms 帧预算（yieldInterval，只能靠 forceFrameRate 调）内干活，超时就主动让出主线程；
		让出后用 MessageChannel 而不是 setTimeout 续命是关键：setTimeout 有约 4ms 的最小节流、粒度太粗，而 postMessage 的 onmessage 作为新宏任务排在下一个 task，能让浏览器在两片之间插入输入和绘制——相当于手写的 requestIdleCallback；
		再配 lane 优先级模型，用户输入这类高优更新可以插队。一句话：从"递归不可中断"变成"可中断的游标遍历"。

- 说说 React 并发特性和 useTransition、useDeferredValue？

		useTransition 把某次 setState 标记为"可打断的过渡更新"，期间保留旧 UI（isPending 可以做 loading 态），适合 tab 切换大列表；
		useDeferredValue 把某个值延后传给耗时的子树，保住输入框不掉帧（受控输入 + 大列表过滤的经典解法）；
		配合 Suspense，目标就一个：输入不掉帧，慢渲染可打断可重试。

- React 18 的自动批处理（Automatic Batching）和之前手动 batchUpdates 有什么区别？

		18 之前只有 React 事件处理器里 setState 会批处理，promise/定时器里的一次一个 render；
		18 起所有场景自动批处理（含异步），flushSync 可以强制同步刷新；
		追问点：批处理不是"合并多个 setState 调用"，是把多个更新排队进同一次 render；函数式更新（prev => next）保证拿到最新值。

- React 19 你用了哪些新特性？use()、Actions、useOptimistic、ref as prop？

		Actions：表单/异步提交的原生流程（useActionState 管 pending/error，useFormStatus 在子组件用）；
		use()：渲染中读 Promise/Context，可以条件调用（区别于 Hook 规则的特殊 API）；
		useOptimistic：乐观更新不用手写回滚三件套了；
		ref 直接当 prop 传（forwardRef 可省）、Context 直接当 Provider、document metadata 可以写 <title> 进组件；
		方向性的大头是 React Compiler（自动细粒度 memo，把手写 useMemo/useCallback 的活儿接走）和 RSC 生态。

- React Server Components（RSC）和传统 SSR 的区别？组件什么时候跑在服务端？

		SSR 是"服务端替客户端组件输出首屏 HTML"，之后还要 hydrate，组件代码照样发给浏览器；
		RSC 是组件只在服务端执行（可以直接查库、读文件），产物是序列化的 UI 流，不进客户端 bundle、不需要 hydrate——所谓"零 JS 组件"；
		'use client' 标记交互边界，默认在服务端。收益是首屏体积和数据就近；代价是心智模型变复杂（两种运行时 + 缓存层）。Next.js App Router 把这条路线产品化了。

- Next.js App Router 的渲染模式（SSR/SSG/ISR/流式渲染）怎么选？缓存策略踩过坑吗？（阿里）

		纯静态内容（营销页/文档）SSG + CDN；强个性化 SSR；介中间 ISR（revalidate）；默认姿势是 RSC + Suspense 流式渲染（loading.tsx / generateStaticParams）；
		坑基本都集中在 App Router 的多层缓存：fetch 结果默认缓存（15 起要主动 cache/no-store 表态）、路由缓存、完整动态页要 dynamic = 'force-dynamic'；
		"改了数据页面不更新"这题能讲清楚，缓存这块就算过关。

- 虚拟列表（Virtual List）怎么实现？长列表无限滚动白屏怎么优化？

		核心计算：总高 = 条数 * 预估行高；可视区起/止 index 由 scrollTop 和容器高算出；只渲染可视区 ± 缓冲区若干条，transform/absolute 摆到对应偏移；
		不定高列表用"预估 + 渲染后测量校正偏移表"（react-virtuoso、@tanstack/virtual 的思路），或者约束内容高度上限；
		白屏优化：加大 overscan、图片先占位骨架、提前预取下一页、AI 对话流场景还要处理流式输出时的高度抖动和"贴底"逻辑（用户上滑就不强制贴底）。

- Vue3 的 ref 和 reactive 区别？解构为什么会丢失响应性？

		reactive 是用 Proxy 包整个对象（只能对象），ref 是 .value 包任意值（基本类型只能用 ref）；模板里 ref 自动解包，js 里要 .value；
		解构 reactive 拿到的是普通值的引用，脱离了代理链路，所以要用 toRefs 或者不拆；
		响应式的本质是"读时收集依赖、写时触发更新"，值一旦离开代理，读它就不经过 get 陷阱了。把依赖收集讲清楚，这题就稳了。

- 说说 Vue3 的 Composition API 解决了什么问题？和 React Hooks 思路上的异同？

		解决 Options API 两大痛点：一个功能的 data/method/watch 分散三处、跨组件复用只能 mixin（来源不透明、易冲突）；setup 里逻辑按关注点聚合，还天然对 TS 友好；
		和 Hooks 同的是函数式组织逻辑；不同的是：Vue 的 setup 只执行一次、响应式是真实可变对象（解构自由但要守规矩）；React 每次 render 重跑函数、状态是不可变快照（所以有依赖数组和调用顺序限制）；
		两边的 diff 策略差异（编译期感知 vs 运行期 memo）也是从这个根基长出来的。

- Vue3 编译期做了哪些优化？（静态提升、Patch Flags）

		静态提升：纯静态节点提出 render 函数外，不重复创建 vnode；
		Patch Flags：编译期给动态绑定打“位标记”（TEXT/CLASS/STYLE/PROPS/FULL_PROPS 等，可用 | 组合、用 & 判断），运行时只比对被标记的点；一旦某块带 dynamicChildren，diff 进入 optimized mode，直接跳过静态部分；
		几个源码级细节：PROPS 会额外带一个 dynamicProps 数组记录哪些键可能变（更新时不用纠结被删的 prop）；fragment 用 STABLE/KEYED/UNKEYED_FRAGMENT 决定要不要 diff、要不要按 key 建映射；静态提升出的节点带 CACHED，连 hydration 都跳过整棵子树；遇到手写 render 或 cloneVNode 则置 BAIL，退回全量 diff；
		Block Tree 把动态节点收集成扁平数组，更新复杂度只跟“动态节点数”相关，而不再跟整棵树规模挂钩；
		再加事件缓存、style/class 静态合并。Vue3 把 diff 优化做在编译期，这是它和 React 运行期 memo/lane 思路最大的分野。

- Vue 的 diff 和 React 的 diff 有什么核心区别？（双端比较 vs 最长递增子序列）

		Vue2 是双端指针向中间逼近；Vue3 新子节点先处理头尾的稳定片段，中间乱序部分建立索引后用"最长递增子序列"求最少移动；
		React 靠 key + 单次遍历（无 key 直接重建），乱序用 map 查旧节点位置，不做 LIS——它把性能押在调度和 memo 上；
		更深层：Vue 的模板编译期能标注动态性（见上题），React 的 JSX 是运行时构建 vnode，信息量先天不足。

- Pinia 相比 Vuex 改进了什么？

		去掉了 mutations（只有 state/getters/actions，异步直接写 action）、TS 推导一流、组合式 store（setup 语法）、多 store 自由互相调用、体积更小、devtime 照样支持；
		Vuex 4 之后基本没人投入了，Vue 官方的推荐位从 2019 年就给了 Pinia。

- Zustand、Jotai 这类轻量状态库为什么流行？和 Redux 怎么选？

		共同点：没有 action/dispatch 仪式、不可变直接 set、样板代码少一个数量级、体积 KB 级（Jotai 是原子化按订阅渲染，Zustand 一个 hook 读全局）；
		 Redux 阵营现在也走 Redux Toolkit（样板砍半），但选型逻辑变了：服务端数据交给 React Query/SWR，客户端只剩 UI 状态，轻量库刚好够用；
		RTK 留给中间件生态（saga）、团队规范和超大型应用的场景。"全局大 store 变小、状态就近 + 服务端缓存分离"是这两年的主趋势。

- 你们项目是 React 还是 Vue？重新选型你会怎么选，为什么？

		开放题，考的是权衡不是站队：团队构成（React 学习曲线陡但全栈化/海外人才多）、生态（React 的 RN/RSC/高质量三方，Vue 的国内中后台生态）、交付节奏（Vue 上手快）、历史资产（组件库、构建链迁移成本）；
		答出自己项目里真实踩过的坑（比如 Vue 的 mixin 冲突、React 的依赖数组地狱）比背结论值钱。


- React 的 key 到底解决什么问题？为什么"用 index 当 key"在列表会重排时是 bug？

		key 是 React 在 diff 时识别"同一个元素"的稳定身份，不是渲染优化开关。虚拟 DOM 逐项比较时，靠 key 判断新旧列表里哪项是同一个，决定复用/移动/销毁；		用 index 当 key 的问题是"身份跟着位置走"：列表插入/删除/重排后，同一 index 指向了不同数据，React 以为还是同一个组件，于是复用了错误的 DOM 和组件 state——表现为输入框内容错位、动画错乱、受控组件串值，这些就是"用 index 出 bug"的真面目；		正确做法：用数据自带的稳定唯一 id；没有 id 就在数据进入列表前生成并固定，绝不在 render 里现算（每次变反而更糟）；静态列表完全不动才可以不写 key。

- useEffect 的依赖数组为什么这么容易被误用？说说闭包陷阱、effect 触发时机、和"从 Props 派生状态"的关系。

		依赖数组本质是一个"手动维护的缓存 key"，React 靠 shallow compare 数组项决定要不要重跑 effect——漏写依赖，effect 里读到的是旧闭包捕获的值（stale closure），不是"React 忘了"，是你没把它列进依赖；eslint 的 exhaustive-deps 规则必须开着；		时机：useEffect 在浏览器绘制之后异步跑（不阻塞渲染），需要"绘制前同步读布局/改 DOM"用 useLayoutEffect；每个 effect 应做一件事，把不相关的逻辑拆开，否则清理函数会互相牵连；		最常见的误用是"用 effect 做本可以渲染期算的派生"——能从 props/state 直接算出来的值不要 setState + effect 存一遍（多一次渲染、还容易不同步），要缓存用 useMemo；真正需要 effect 的只有"和外部系统同步"（订阅、手动改 DOM、请求第三方）。

- 状态管理在 2026 年怎么选？Redux/Zustand/Jotai/TanStack Query/Context 各自的定位。

		先把两类分开，这是这题的关键：服务端状态（后端数据）归 TanStack Query/SWR 管（缓存、去重、失效重取、乐观更新它内建），客户端状态（UI 态、跨组件共享且 Query 覆盖不到的）才轮到 Redux/Zustand/Jotai；很多人把接口数据塞进全局 store 自己造轮子，是概念错位；		客户端状态里：Context 适合低频更新的全局值（主题、登录用户、i18n），缺点是 value 一变所有 consumer 重渲染、要做拆分和优化；Zustand 外部 store + selector 订阅，样板少、性能好，是现在中小项目默认；Jotai 原子化适合状态碎片化、组合多的场景；Redux Toolkit 留给大团队、要中间件规范和 DevTools 时间旅行的企业级；		选型话术：先看数据归属，再看更新频率和团队规模，别为"用不用得上"上 Redux。

- 组件设计：什么是"受控 vs 非受控"？怎么设计一个两种都支持的组件？

		受控 = 值由父组件的 state 持有、组件只渲染 value + 回调 onChange（数据单一来源，父组件随时能读/改/校验）；非受控 = 值在组件内部自己管，父组件通过 ref 命令式取值（省事，但值脱离 React 数据流）；		两都支持的写法：传了 value/onChange 就走受控、不传就用内部 state 兜底（uncontrolled）；实现要点是"prop 提供了就尊重 prop，没提供才用内部"，再统一一个 setValue 决定要不要同步内部 state——这就是 radix / rc 那套 useControllableState 的思路；		加分：把"什么时候该受控"说清——需要外部驱动/联动/即时校验就受控，纯独立表单提交时读一次就非受控，能降低无谓重渲染。

- SSR / RSC / 流式渲染这一堆概念，2026 年 Next.js 项目里到底该怎么理解？

		先分层：SSR（每次请求服务端渲染 HTML，首屏快但每次都要算、要水合）；SSG/ISR（构建或增量生成静态）；hydration 是为把静态 HTML 变成可交互 React 树，代价是主线程再跑一遍、下载组件 JS；这带来的"能看不能点"的空窗和 JS 体积是 SSR 的老问题；		RSC（Server Components）换了个维度：组件只在服务端跑、产物是序列化的 UI 不是 JS，直接把数据获取留在服务端 + 减包子，不用等 hydration 就能出内容；客户端交互部分用 'use client' 边界切出来；流式（Streaming + Suspense）让 shell 先出、慢区块后到，改善 TTFB/LCP；		实战判断：不是全 RSC，而是"数据重、无需交互的上文用 Server Component，交互岛用 Client"；Next 的 App Router 缓存（fetch/router cache）是另一堆坑来源，答题时点一句"要理解它的缓存层否则数据会陈旧"就是实战过的信号。

- React hooks 的底层实现原理？为什么多次渲染还能拿回上一个状态？（腾讯/米哈游面经）

		每个组件 fiber 上挂着一条 memoizedState 链表，hook 按调用顺序对应链表节点：首次渲染按顺序创建节点，之后渲染按顺序走链表取回——所以"调用顺序"就是 hook 的身份，这就是不能写条件语句的机器级原因；
		useState 的值存在节点里，setter 触发的更新先进节点的待处理队列，渲染时再算出最终值；useRef / useEffect / useMemo 是同一条链表上的不同节点类型，只是 payload 和处理逻辑不同；
		到这个层次已经能过，高分答案再加两点：为什么用链表不用数组（节点数量不固定、O(1) 追加、跨渲染复用语义清晰）；以及组件更新时 hook 状态怎么跟着走——reconcile 克隆 fiber 时整个 memoizedState 链一起带过去；

- Fiber 节点大概是什么样的结构？为什么它能支持中断渲染？（美团面经）

		一个 fiber 就是一条可中断的工作单元记录：type/key 说明它是谁，stateNode 指向真实 DOM 或组件实例，child / sibling / return 三个指针把组件树压成可以单层遍历的链表结构，另有 alternate 指针指向双缓冲的另一棵树；
		render 阶段在 workInProgress 树上纯计算不碰 DOM，产生 effect 标记，commit 阶段按 effect 链表一次性应用 DOM 变更——两阶段的分界线就在这；中断安全性靠双缓冲：随时可以丢弃整棵 workInProgress 树重来，current 树始终是完整可用的；
		时间切片的答法别背概念：reconciliation 被拆成一个个 fiber 级小任务，每帧用剩余时间执行一段，浏览器要回来渲染/响应用户输入时让出，下一帧继续；能说清"中断后凭什么不丢状态"（链表 + 双缓冲 + 副作用延后）就是懂行；

- setState 是同步还是异步？为什么要批量更新？什么时候需要 flushSync 强制同步？（拼多多面经）

		准确说法不是"异步"是"批量"：React 18 之后，无论在事件回调、生命周期还是 setTimeout、微任务里，连续 setState 都会被合并成一次渲染（automatic batching）；想在下一行拿到最新 DOM/状态，用 flushSync 包住这次更新，或者改用函数式更新 setState(v => v + 1)；
		批量的动机：从状态变更到 DOM 更新中间隔着整棵子树的 render 和 reconcile，不合并等于把 O(子树) 的开销乘以调用次数；顺带也避免用户看到中间态闪烁；
		这题最爱连环追问"为什么 setState 之后打印还是旧值"：因为 state 变量是当前这次渲染闭包捕获的快照，setter 只是把更新排进队列，不会改已解构出来的常量；把"闭包快照"讲出来，这串题就全通了；

- React 为什么要拆分成 react 和 react-dom 两个包？（QQ音乐面经）

		分工：react 包是平台无关的核心——组件模型、createElement、hooks 定义、协调算法调度；react-dom 是实现渲染接口的平台适配层，react-native、react-test-renderer、Ink（终端渲染）各自适配各自的目标；换渲染目标不用重写组件模型；
		这个拆分的价值可以用事实检验：第三方能基于它造出新渲染器（react-native-web、react-three-fiber），说明解耦是真的，不是讲故事；Vue 3 后来把 runtime-core / runtime-dom / compiler-dom 拆开，走的是同一逻辑；
		容易顺带追问的相邻问题：JSX 编译后是什么——React.createElement(type, props, ...children) 调用产出的普通对象树（虚拟 DOM），它就是 fiber 的原料；编译器（babel / swc / oxc）只负责把语法变成这些对象；

- 你觉得 React 有什么缺点或者设计上值得商榷的地方？（米哈游面经）

		别开地图炮，答"有代价的取舍"这个框架：第一个代价是隐式数据流——渲染期直接读 state/props，框架不做自动依赖追踪，于是 memo / useMemo / useCallback / 依赖数组全成了"手动挡"，useEffect 依赖误用率高本质上就是这个问题外溢；
		第二个代价是官方边界留白：路由、数据获取、表单这些核心链路官方不管，生态里各派方案各讲各的最佳实践，团队选型和知识折旧成本都转嫁给了使用者；
		第三个才是具体痛点：双树（fiber 树 + DOM）的内存开销、状态全量重新执行的渲染模型、Hooks 带来的首屏水合成本。能把"它换来了什么、为什么多数团队仍觉得值"说完，这题就从吐槽升到了架构评估；

- React 中跨组件传值/联动的方案有哪些？差异和适用场景分别是什么？（字节面经）

		分层报方案：父子用 props / children；深层透传用 Context（注意它的更新会重渲染所有消费组件，适合低频"环境型"数据）；全局业务状态用 zustand / Redux（订阅粒度决定性能）；可分享可回退的状态放 URL；服务端数据交给 TanStack Query 这类缓存层；最后才是事件总线兜底；
		选型的第一性问题是"这个状态归谁管"：服务端数据不该复制进全局 store（两头同步是灾难）、局部 UI 态不该提升到全局（渲染范围爆炸）；能顺手给出"从 props 派生状态"反模式的判断标准（能不能由已有 state 纯计算得到），就是干净的架构感；
		字节的追问一般在 Context 和 zustand 的性能差异：Context 没有 selector，value 一变全体消费者重渲染；zustand 用 hook 订阅切片、浅比较不过就不渲染——这也是"环境配置用 Context、业务状态用 store"这条经验的底层依据；

- zustand 的底层原理是什么？依赖收集和订阅是怎么做的？和 Redux 的本质差异在哪？（字节面经）

		zustand 的本质是"外部 store + useSyncExternalStore"：create 的闭包里持有 state 和监听者集合，setState 浅合并出新对象后通知订阅者；组件通过 useStore(selector) 订阅切片，默认 Object.is 浅比较决定重不重渲染；没有 Provider、没有 reducer 仪式；
		和 Redux 的差异不在 API 风格，在工程模型：Redux 是单 store + action 单一真源，可回放、中心化治理（DevTools、中间件、团队约束强）；zustand 允许多 store 自由组合，上手快约束少，团队大了以后靠约定维持；两者订阅机制倒是一脉相承（react-redux 的 useSelector 和 zustand 的 selector 思路一致）；
		面试官经常把不可变数据串在这题后面：更新必须产生新引用（浅拷贝一层）订阅端才能用浅比较判断变化；手写深层拷贝太累所以配 immer，produce 的结构共享让没改动的分支复用原引用，比较代价就锁在了改动路径上；

- SSR 的原理是什么？服务端渲染完之后，浏览器还要做什么？（字节面经）

		流程：服务端把组件渲染成 HTML 字符串直出（数据请求也集中在服务端做完），首屏可见不等 JS bundle；但这一刻页面只是"看起来能用"，事件、状态都不存在，浏览器还要做水合（hydration）：把组件树"接"到已有 DOM 上，绑事件、恢复状态；
		关键的坑在状态双份：服务端取的数据要序列化写进 HTML（window.__INITIAL_STATE__ 之类），客户端初始化时优先复用它而不是重新请求，否则闪 loading 加双倍请求；序列化要处理 XSS——JSON.stringify 之后得防 </script> 闭合注入；两端渲染不一致就是 hydration mismatch，日期、随机数、window 判断都是经典雷区；
		追问会往现代变体走：流式 SSR 把 HTML 分块推送、骨架先出；RSC 干脆让一部分组件只在服务端跑、不下发对应 JS，水合范围再缩小；SSR 的性能账要算总账——省掉的白屏时间有没有把 TTI 的水合成本还回去；

- 你在真实项目里做过哪些 React 性能优化？性能瓶颈是怎么定位的？（腾讯面经）

		先分层再报手段：编译层（代码分割、路由级懒加载、预加载策略）；渲染层（memo / useMemo / useCallback 切断无效重渲染、状态下沉缩小渲染范围、派生值不进 state、长列表虚拟化）；调度层（useTransition 把非紧急更新降级、useDeferredValue 让大渲染不吃输入响应）；
		手段之前必须有定位：React Profiler 看 commit 火焰图、Performance 面板找长任务，先证明"谁在浪费渲染"再动手；"全页糊 memo"是反方向操作——比较本身有成本，不该断的断不掉、该断的没断；
		真实项目里最值钱的优化往往不在 React 身上：请求串行改并行、接口聚合、图片与资源策略、包体积；答完组件级再补一句"瓶颈经常不在框架层，要先证明它在"，这题就从八股升到了工程判断；

- React 组件报错怎么处理？Error Boundary 捕获不到哪些错误？（米哈游面经）

		Error Boundary 是类组件形态（getDerivedStateFromError 出兜底 UI，componentDidCatch 做上报），包住子树就能在渲染抛错时局部降级而不是白屏；React 官方一直没发 hook 版，实践用 react-error-boundary 这类封装；
		捕获盲区要背准四类：事件回调里的错误（要自己 try/catch）、异步任务（setTimeout / Promise）、服务端渲染阶段、以及边界自身渲染抛出的错；所以线上方案必然是双轨——Error Boundary 管组件树，window.onerror + unhandledrejection 管其余；
		米哈游面经后面还跟着调试题，一起记：Sources 面板用条件断点、Blackbox 掉框架堆栈避免单步进 React 内部、Profiler 的 highlight updates 看重渲染范围；这类"手上有没有活"的细节最能和背题的人拉开差距；

## <a name='eng'>工程化与构建</a>

- 你为什么从 webpack 迁移到 Vite（或反过来）？Vite 开发环境秒启动的原理？

		原理两条：（1）dev 直接用浏览器原生 ESM，按需编译——不打包，启动时不建全量依赖图，import 链条走到哪编到哪；
		（2）依赖预打包用 esbuild（Go）把 CJS/零散依赖合成 ESM 并缓存，冷启动只做这一件事；HMR 按文件粒度，不随项目变大而变慢（webpack 后期全量 rebuild 是最大痛点）。
		反向迁回 webpack 的理由一般是：老项目动态 require/自定义 loader 太多、需要 webpack 特有插件、产物一致性要求高。
		面试要说"取舍"，别只说"谁碾压谁"。

- Vite 为什么开发用 esbuild、生产构建用 Rollup？Rolldown 了解吗？

		esbuild 快，但代码分割和产物质量（tree-shaking、chunk 一致性）不如 Rollup 成熟，所以 dev 用它做转换和预打包、build 用 Rollup 保质量；
		代价是 dev 和 prod 产物不完全一致（依赖优化边界、CSS 顺序），会出"dev 没事 build 出事"的诡异 bug；
		Rolldown 是用 Rust 写的高性能打包器，官方定位是 Rollup 的直接替代品（drop-in replacement，兼容现有 Rollup 插件）；Vite 要迁到它的核心动机，是把"dev 用 esbuild 预打包 + build 用 Rollup"这套双引擎统一成一个，从根上消除产物不一致和链路复杂度，还顺带带来高级分包控制、内建 HMR、Module Federation 这些 Rollup/esbuild 没有的能力；
		落地路径是先以 rolldown-vite 包提供（在 package.json 里把 vite 别名成 npm:rolldown-vite 即可替换体验），Vite 后续版本再把默认打包器切到 Rolldown（2026 年已进入默认阶段）。答到"为什么要统一引擎"这一层，比只背"esbuild 快、Rollup 稳"高一个档次。

- Rspack 和 Turbopack 的定位分别是什么？老 webpack 项目迁移成本主要在哪？（头条）

		Rspack：Rust 实现、兼容 webpack 生态（大部分 loader/plugin 直接可用），定位是"存量 webpack 项目无痛换引擎"，字节大规模落地后开源；
		Turbopack：Vercel 出品、只服务 Next.js、增量计算架构，不追求兼容 webpack，面向新项目；
		迁移成本看三样：依赖 webpack 内部对象的自定义插件、CommonJS 风格的动态 require、DefinePlugin/复杂 alias。验证靠产物 diff + 全量 e2e，不是"能跑就行"。

- Babel 和 SWC 的区别？为什么 SWC 快这么多？

		SWC 用 Rust + 原生执行，没有 GC、天然并行；Babel 是 JS 单线程跑 AST，对象开销大；官方数字：转译快 20x、压缩快 4.5x；
		代价：Babel 插件生态没法全兼容、个别边缘转译行为有差异；
		现在的分工：TS/JSX 转译基本交给 SWC / esbuild（Vite、Next、Jest 都接了），Babel 退守装饰器、宏和存量插件。

- pnpm 为什么省磁盘、装得快？软链接、硬链接和内容寻址存储讲一下。

		全局 content-addressable store（按文件 hash 存），项目里通过硬链接指到 store，不同项目共享同一份物理文件；
		node_modules 是符号链接结构：.pnpm/<pkg>@version 放真实目录，顶层再软链出去，没声明的包进不来——幽灵依赖被结构性禁掉；
		快是因为命中 store 直接链接、不重复下载解析；
		坑：个别老包拼死路径的 require 会找不着、非扁平结构兼容问题。workspace + catalog（pnpm 9+ 统一版本声明）现在是 Monorepo 标配。

- npm / yarn / pnpm 怎么选？lock 文件冲突怎么解决？

		2026 年基本 pnpm 优先：确定性好、workspace 成熟、磁盘友好；yarn berry 的 PnP 激进但接手成本高；npm 胜在零额外依赖；
		lock 冲突的正解不是手工合并（语义上合不了）：基于远端 checkout lock 后重新 install 让它自己补全，或用 overrides 收敛版本；
		团队层面靠 CI --frozen-lockfile 校验 + corepack / packageManager 字段锁包管理器版本，从根上少冲突。

- Monorepo 怎么落地？pnpm workspace + Turborepo 用过吗？和 git submodule 什么关系？

		一个 git 仓库 + pnpm workspace（workspace: 协议引内部包）+ Turborepo/Nx 做任务编排：按依赖拓扑构建 + 内容 hash 缓存（本地/远程），CI 时间大头被缓存吃掉；
		版本发布配 changesets（版本清单 + 自动发版 PR）；
		git submodule 是"仓库引用仓库"的指针机制，和 Monorepo 是两个方向的事，别混用；
		真正的难点：CI 矩阵、权限隔离、发布节奏一致性。

- Tree Shaking 的原理？sideEffects 配置不起效通常是什么原因？

		基于 ESM 静态 import/export 结构，bundler 标记未被引用的导出，交给 minifier 消除死代码（CJS 结构上做不到）；
		不生效的常见原因：包没发 ESM 入口（混进了 CJS）、package.json 的 sideEffects 没配或没排除 css、引入了带顶层副作用的模块（polyfill、register 类）、babel 把 ESM 转成了 CJS（modules:false 忘配）；
		排查用 --stats / source-map-explorer 看产物里到底被拖进来了什么。

- 代码分割有哪些手段？路由懒加载之外还做什么？怎么处理预加载？

		路由级 dynamic import 是基线；再细：组件级 lazy + Suspense fallback、弹窗/详情这类"二次交互"按需、大依赖（图表/编辑器）单独 split 或换轻量方案；
		构建层 splitChunks/advancedChunks 分 vendor、按更新频率拆 core/update 两类缓存；
		预加载别忘：路由空闲时（requestIdleCallback）预取下一页、hover 链接时 import；拆太碎首屏请求瀑布反而更慢，要按指标下刀。

- SourceMap 原理？线上报错如何还原堆栈，又不把 map 暴露到公网？

		map 文件是 VLQ 变长编码的映射表（生成列、源文件、源行列、名字），还原时二分查找；
		生产做法：构建时上传 Sentry/内部平台后删除产物中的 map；或 sourceMappingURL 指向带鉴权的私有域 / X-SourceMap 头；
		配 release 和 artifact 对齐版本，不然一个 chunk 对多版本 map 就乱套了。

- 前端监控怎么做？JS 异常、性能、用户行为采集，Sentry 用过吗？

		异常：window.onerror / unhandledrejection + 框架边界（ErrorBoundary、Vue errorHandler）；跨域脚本默认拿不到详情，要 script crossorigin + CORS 响应头；
		性能：PerformanceObserver 采 LCP/INP/CLS，区分实验室（Lighthouse CI）和真实用户（RUM）；
		行为：面包屑（路由/点击/请求环形缓冲）+ 录制回放（rrweb）定位现场；
		上报走 sendBeacon 防止页面关闭丢包、采样和聚合降量。Sentry 是现成方案，自建重在数据归属和成本，架构上就是这一套。

- 微前端解决什么问题？qiankun、wujie、Module Federation 的 JS 隔离原理分别是什么？

		解决的是巨型单体团队的协作内耗、异构技术栈渐进迁移、多应用整合——注意它不是性能方案！
		qiankun：single-spa 之上。JS 沙箱有三档——SnapshotSandbox 激活/失活时遍历 diff window 属性（只允许单实例、给 IE11 这类老浏览器兜底）、LegacySandbox 用一层 proxy window、ProxySandbox 给每个应用各建一个 proxy（现代浏览器，也是唯一能多实例并存的方案）；
		样式隔离两档——strictStyleIsolation 用 Shadow DOM（隔离最彻底，但第三方把弹层挂到 body 会失效）、experimentalStyleIsolation 给每条选择器加 scoped 前缀改写（宽松些）；
		wujie：用 iframe 做 JS 执行环境（天然隔离全局变量）、却把 DOM 渲染进主文档里的自定义元素（WebComponent）——等于“iframe 的隔离 + 同文档的渲染”两头好处都拿；子应用资源由主应用用 axios 拉回来再拼成 blob: URL 注入，避开跨域和二次请求，样式也能靠同文档共享；通信走 props / window 直通；
		Module Federation：构建运行时的共享模块（不是容器隔离），同一套 webpack/Rspack 体系内互相同步依赖；
		高频追问：公共依赖多实例（React 双实例报错）、路由同步、登录态打通、子应用加载性能。

- 你们的 CI/CD 流程是什么样？前端发布如何做到秒级回滚？

		典型链路：MR -> CI（lint/test/build，产物带 contenthash）-> 推静态目录或镜像 -> 灰度发布（按权重/用户/头）-> 全量；
		秒级回滚的本质是"版本化 + 入口切换"：静态资源按版本目录全量保留，回滚只是把入口（index.html 指向的版本）切回去，不用重传；
		SSR/BFF 这类服务端场景做不到这么轻，也要配快速切流。回滚演练过才算数。

- CDN 缓存策略怎么定？为什么 index.html 不能强缓存？hash 文件名解决什么问题？

		带 hash 的文件名内容不可变 -> max-age 一年 + immutable 强缓存；
		index.html 每次发布都可能变 -> 只能协商缓存（no-cache 或 max-age=0），强缓存了新版本就永远下不来；
		本质是"可变的入口 + 不可变的资源"：入口当版本指针（发布/回滚都动它），资源吃缓存；
		追问：hash 依赖构建可复现（同 commit 同产物）；旧 hash 资源要留一个发布窗口再清理。

- Docker + Nginx 部署前端，gzip/brotli、缓存、history 路由 fallback 怎么配？

		brotli 优先（CDN 支持时），更省 CPU 的做法是构建期就压好、nginx gzip_static on 直接发 .gz；
		缓存按上面策略配 expires；
		history 路由 try_files $uri $uri/ /index.html——但静态资源 404 别也回落 index.html（JS 请求拿到 HTML 会报 MIME 错，这个坑很经典）；
		多阶段构建（node 编译 -> nginx 运行）把镜像从几百 MB 压到几十 MB；容器里注意 SIGTERM 优雅退出。

- 包体积优化你做过什么？指标和手段分别说说。（gzip 后体积、依赖分析、按需引入）

		指标：主包 gzip 后体积、首屏总传输量、LCP；手段按投入产出排：
		大依赖替换（moment -> dayjs、lodash 整包 -> 单包/原生、图标库全量 -> 按需）、代码分割 + 预加载、polyfill 按 browserslist 注入、图片字体子集化（webp/avif）、确认 tree-shaking 真的生效、bundlephobia 查依赖成本；
		也要会算边际：为省 5KB 多一次请求可能反而慢，这题答"取舍"比答"清单"高级。

- Monorepo 在 2026 年怎么落地？pnpm workspace + Turborepo/Nx 各解决什么，什么时候不该用？

		Monorepo 解决的是"多包协同"：依赖版本统一、跨包改动原子提交、复用配置和 CI；用 pnpm workspace 做包管理和内部软链（catalog 统一版本），用 Turborepo/Nx 做任务编排——核心是增量 + 远程缓存（只构建变更影响到的包，命中的从缓存拉），把大仓库 CI 从全量压到增量；		Nx 更重（依赖图分析、code generators、插件生态），Turborepo 更轻（拓扑 + 缓存，配置即用）；		什么时候别用：单产品单仓库、团队小、没有复用诉求——Monorepo 引入的工具链复杂度和"一次 CI 跑全仓"的耦合成本不划算；也别把不相关的项目硬塞进来；权限和发布节奏差异大的多产品线，Polyrepo 反而清爽。

- 前端 CI/CD 现在怎么做才算合理？构建产物、缓存、发布策略、回滚说说。

		CI 流水线：装依赖（锁文件 + 缓存 node_modules/pnpm store）-> lint + typecheck + test -> build -> 产物体积对比和视觉回归；关键是"该挡的在 PR 阶段就挡"，别让坏代码进主干再救；构建依赖缓存命中能省一半时间（turbo/nx remote cache 或 actions/cache）；		CD：构建产物 hash 命名 + index.html 协商缓存（配合前面 CDN 缓存策略）、产物传 CDN/OSS；发布策略用灰度/金丝雀（按用户/流量比例放量）和蓝绿（两套环境秒切），前端最实用的是"新版本先小流量 + 保留旧版本随时切回"；		回滚：产物多版本共存 + 配置开关切指针（别覆盖式部署，覆盖就没法秒回滚）；配 source map 上传到监控（Sentry）让线上报错可读栈。

- 前端监控体系怎么搭？错误监控、性能监控、行为日志三条线分别怎么做？

		错误监控：全局兜底（window.onerror 抓同步、unhandledrejection 抓 Promise、资源加载 error 抓脚本/图片 404、框架 ErrorBoundary 抓渲染错），配 source map 还原栈、错误指纹去重（同类合并防刷屏）、采样上报防打爆；		性能监控：真实用户 RUM 采 Core Web Vitals（PerformanceObserver，75 分位），和发布版本、地域、设备维度关联才能定位回归；错误和性能都按 release 打标才能看"这次发布有没有变差"；		行为日志：用户操作路径（点击、路由、关键动作）做"复现上下文"，报错时能带回崩溃前 20 步；三条线要用同一个 session/trace id 串起来，否则线上问题只能各看一片；采样和脱敏（别传 PII）是底线。

- 前端测试到底测什么？单测/集成/E2E 的投入产出怎么权衡？

		遵循测试金字塔但按前端现实调：纯函数、复杂逻辑、工具层用单测（Vitest）快准稳；组件行为用集成测试（Testing Library，按"用户能看到的"查 DOM、别测实现细节）；关键业务路径用 E2E（Playwright）覆盖登录/下单这类走通才算数的链路，数量要少而稳；		不追求覆盖率高，追求"改到就会挂的关键点有测试"；前端最脆的是"测了实现细节的重构即崩"，所以断言对着用户可感知的行为和契约（接口、渲染结果），不对着内部 state/私有方法；		E2E 要治理 flaky（等待用 web-first 断言不用 sleep、测试间隔离数据），否则 CI 红了没人信就等于没测。

- 依赖治理：你怎么控制一个前端项目的依赖风险？

		入口先卡：加依赖要看周下载量、维护活跃度、license、体积（bundlephobia）、有没有被 tree-shake——能用原生/已有库解决的不新增；npm 幽灵依赖靠 pnpm 的严格 node_modules 根治（见 pnpm 相关题）；		安全：lock 文件必须提交、CI 跑 npm audit / socket 类工具查供应链、锁传递依赖版本（overrides/resolutions）防上游偷偷升级、警惕 typosquatting 和 postinstall 脚本（CI 可 --ignore-scripts）；		升级：用 Renovate 自动开 PR 分批升，小步升配合测试快速定位是哪次升级引入的问题；重大依赖（框架、构建）升级单独立项评估——把"升级"变成常态小动作，而不是三年一次的考古。

- webpack 插件机制的原理？你们为什么要自定义 webpack 插件？（字节面经）

		原理是 tapable：compiler 把构建生命周期挂成一串钩子（environment → entryOption → thisCompilation → compilation → make → seal → emit → afterEmit…），插件对象只需实现 apply(compiler)，往对应 hook 上 tap 回调；loader 管单个文件的内容变换，plugin 管构建流程的干预，边界就在这；
		自定义插件的场景都围着 compilation 对象转（modules、chunks、assets 都挂它身上）：构建期注入全局常量、产物后处理（版本注释、CDN 前缀改写）、构建质量卡点（体积超限告警、依赖越界扫描）；
		真实追问是"为什么非要自己写"：因为需求卡在官方插件没覆盖的生命周期点上，说得出具体的点才立得住；顺势还能答迁移视角——Vite 插件改用 Rollup 风格 hook 是为了兼容 Rollup 生态，团队从 webpack 迁走时自定义插件往往就是最大迁移成本项；

- 模块联邦（Module Federation）和 npm 包的区别？为什么它适合微前端做共享？（拼多多面经）

		npm 是编译期共享：改动要发版→下游安装→重新构建，一次升级全链路重发；模块联邦是运行时共享：主应用运行时加载远程模块暴露的组件，shared 依赖在运行时协商单例（React 只留一份），版本兼容也是运行时的事；
		它撑住了微前端"独立发布"的叙事：子团队发自己的 remote，主应用零改动，用户侧平滑升级——发布权按团队切分的底座就是这个；代价也要讲：类型检查跨不过运行时边界、共享依赖版本是隐式契约、出问题要跨仓库联查；
		结论级的选型口径：稳定、通用、版本可以慢的东西走 npm（基础库、三方依赖）；团队间实时共享的业务组件走模块联邦；一句话"编译期共享和运行期共享解决的是不同问题"，这题就答到位了；

- 性能优化专项交给你，"首屏时间"怎么定义、怎么统计？（字节面经）

		先对齐口径再谈优化："首屏"没有物理标准，工程上两条线——实验室口径（导航起点到 FCP / LCP，或自定义"首屏内容全部渲染完成"打点）和真实用户口径（RUM 上报，看 LCP 的 P75 分布，不用均值）；
		统计实现：PerformanceObserver 订阅 LCP / CLS / INP，navigation timing 拆 DNS / TTFB / 渲染各段占比，关键元素用 Element Timing API 标记；早期"首屏时间"靠截屏比对，现在基本被 LCP + 自定义打点替代；
		专项方法论是这题的本体：量化目标（LCP P75 从 X 到 Y）→ 拆瀑布找大头（TTFB 问题归服务端/边缘节点，加载问题归资源策略，渲染问题归 JS 体积和执行）→ 灰度 A/B 验证收益 → 线上监控设劣化告警；背优化清单不如把这条闭环讲顺，字节的追问路径就是照着闭环走的；

- 前端错误监控在什么时机、用什么通道上报？（QQ音乐面经）

		采集面五条轨：window.onerror（同步执行错误）、unhandledrejection（Promise 错误）、资源加载错误（捕获阶段 error 事件或 PerformanceResourceTiming）、React Error Boundary（组件树渲染错误）、接口异常（fetch / axios 拦截器）——少一条就有监控盲区；
		上报通道：首选 sendBeacon（页面卸载也发得出、不阻塞主线程），降级用 1x1 GIF（天然跨域无 CORS 成本），大流量走批量队列 + fetch keepalive；时机是本地缓冲、定时批量合并、visibilitychange 变 hidden 时冲刷，配合错误指纹聚合限流防风暴；
		QQ音乐面经这条线的深水区在"能不能定位"：source map 不能传公网（上传到监控平台私有解析、按 release 版本匹配）、上报要带会话面包屑（最近路由和关键操作）否则无法复现；能把"采集→上报→还原→定位"讲完整才是这套题的满分线；

- 前端埋点怎么实现？团队里怎么管埋点质量？（字节面经）

		三种采集模式：声明式（DOM 挂 data-log 属性 + document 级事件委托，改版不丢埋点）、命令式（代码里 track 调用，语义精确但侵入）、全埋点（自动录点击流和曝光，覆盖广但数据脏）；生产上基本是"声明式管点击曝光、命令式管业务事件"的混合；
		工程细节：SDK 本地排队（IndexedDB / localStorage 持久化，断网不丢）、批量合并、sendBeacon 兜底页面关闭；曝光的判定用 IntersectionObserver（可视面积阈值 + 停留时长），元素进 DOM 不等于曝光；
		管理的分量大于实现：埋点需求进评审和版本管理（点位表）、SDK 按元数据 schema 校验字段、上线看量级和完整度监控——字节的追问往往是"怎么保证不多埋不漏埋"，答案在流程（点位生命周期管理），不在代码；

## <a name='ai'>AI 时代的Web工程实践</a>

- Workflow 和 Agent 的区别是什么？常见的工作流模式有哪些？（Anthropic 官方总结）

		Anthropic 在 Building Effective Agents 里给的划分：Workflow 是 LLM 和工具被预定义代码路径编排；Agent 是 LLM 动态决定自己的流程和工具使用。一句话：路径谁定，代码定的是 Workflow，模型定的是 Agent；
		常见模式按复杂度递增：prompt chaining（拆步骤串联，中间可加程序化 gate）、routing（先分类再进专用分支）、parallelization（sectioning 分段 / voting 多路投票）、orchestrator-workers（中心 LLM 动态拆子任务派工，编码类任务常用，子任务不可预知）、evaluator-optimizer（生成-评估循环）；
		官方核心建议：先找最简单的方案，能单次调用+检索+few-shot 解决就别上 agent——agent 是拿延迟和成本换任务表现，没有明确收益就别换。这题答"什么场景不该用 agent"比背全模式更加分。

- 什么是上下文工程（context engineering）？为什么说上下文是稀缺资源？compaction、笔记、子 agent 各解决什么问题？

		官方口径：context 是有限资源、边际收益递减——token 越多，模型从窗口里召回信息的准确率越低（context rot，所有模型都有，只是衰减陡峭程度不同），模型有类似人类工作记忆的"注意力预算"，每个新 token 都在消耗它；
		长任务的三个官方手段：compaction（接近窗口上限时把对话高保真摘要、重启新窗口，最安全的第一刀是 tool result clearing——历史工具调用的原始输出清掉）；structured note-taking（agent 把状态写到窗口外的文件，如 to-do / NOTES.md，之后再拉回来，Claude 玩 Pokémon 上千步靠这个维持目标感）；sub-agent 架构（子 agent 干净窗口干脏活，只回传蒸馏摘要）；
		指导原则一句话：找到"最小高信号 token 集合"。能把这句话说出来，比背一串名词强。

- CLAUDE.md / AGENTS.md 这类规则文件应该写什么、不该写什么？为什么说模型外面那层"壳"（harness）才是工程重心？

		harness 是我理解的 2026 年最重要的认知转变：模型不可修改，你能工程化的是它外面那层壳——系统提示与规则文件、工具集与反馈回路、上下文管理（压缩/笔记/检索）、会话与子 agent 生命周期；"prompt engineering 在变成 context engineering"说的就是这个；
		规则文件每次会话全量注入，是开销不是免费午餐。该写：模型自己探索不出来的项目事实——构建/测试命令、目录约定、规范编号、"不要动 X 文件"这类否定式规则、提交纪律；不该写：模型本来就知道的通用知识、和代码显而易见的描述。规则越多单条权重越低，关键规则会被淹没；
		我自己的判据：这条规则删掉后模型会不会重复犯错——会才留，不会就是噪声。每 3-6 个月该复审瘦身一次。

- 不同模型工具（Claude Code / Cursor / Codex 等）能力差异很大，同一套工作流怎么做到跨模型一致？

		我实际维护过三端，差异在"资产承载能力"：Claude Code 有 skill 工具、.claude/commands/ 斜杠命令、hooks；Cursor 主要是 rules + 显式 Read SKILL.md，没有内置斜杠命令；Codex 是根 AGENTS.md 自动注入，skills 要从仓库 mirror 安装到 ~/.codex/skills；
		工程做法：资产（规则/命令/skill）以仓库为 single source of truth，写脚本 publish 到各端、CI 跑 parity 校验（改一边漏一边是最常翻的车）；设计工作流按"最小公约数"来——假设模型只会读文件、执行命令、按文档步骤走，平台独有能力（hooks、subagent 编排）只做增强不做依赖；
		还要承认行为差异：同一份提示在三端表现可能差很多，这只能靠 eval 和实际使用暴露，别指望文档。

- Claude Code 的 hooks 解决什么问题？和把规则写进 CLAUDE.md 有什么本质区别？权限控制怎么做？

		hooks 的本质是确定性：在工具调用的生命周期节点（PreToolUse/PostToolUse/SessionEnd）强制插入检查，把"希望模型记得做"变成"必然会执行"。我仓库里配了 Write/Edit 后 UTF-8 检测、SessionEnd 写回提醒——这些事写进规则文件模型心情不好就跳过；
		规则文件是概率生效（进上下文，可能被稀释、被遗忘），hooks 是确定生效（不进上下文，是代码）。这是"提示"和"程序"的区别，也是 harness 里 feedback control 那一环；
		权限分级：读放开、写确认、危险命令 deny；原则是用 allowlist 不用 denylist——你永远禁不完模型能想出来的危险操作。hook 自身要轻、失败要响、别自动改文件，否则钩子变成新的故障源。

- sub-agents 和 skills 分别解决什么问题？为什么说 sub-agent 的价值是上下文隔离而不是"多几个人"？

		sub-agent 第一价值是上下文隔离：子 agent 用干净窗口做深度探索（可以烧掉几万 token），只回传 1-2k 的蒸馏摘要，主对话不被搜索垃圾污染；官方 multi-agent research system 的数据是在复杂研究任务上显著优于单 agent。"多几个人"只是表象，买的是注意力预算；
		skill 解决"知识按需加载"：把规范/用法沉淀成带描述的文档，匹配到场景才进上下文，这就是 just-in-time 检索和渐进式披露的落地——对比之下把所有规范塞进全局规则文件，就是在稀释注意力；
		什么时候用什么：问题出在"上下文被污染/不够用"上 sub-agent，出在"缺项目知识"上沉淀 skill。

- 老仓库/大仓库里让 AI 改代码，怎么避免它乱改？验证手段怎么闭环？

		先想清楚根因：老仓库里 AI 改错代码，多数不是模型笨，是隐性知识没显性化——构建命令、"这个目录是全局约定不能动"、"改 XML 必须同步 Mapper"，这些在老人脑子里，模型不知道就只能猜；所以第一步是把仓库契约写进规则文件；
		第二步给验证手段：编译、单测、lint、截图对比，最好有 git worktree 隔离（多任务并行互不覆盖，我们用一个 new-task 脚本生成任务工作树）；"先探索再动手"可以直接写进规则——让模型先 grep/读文件建立心智模型，别拿到需求就输出 diff；
		第三步才是提示技巧。顺序反了就是网上那些"AI 改崩我仓库"帖子的剧本。

- AI 生成的代码你怎么 review？和 review 人写的代码有什么不同？"测试先行"在 AI 时代为什么反而更重要？

		AI 代码最难防的是"完成态假象"：语法全对、看着做完了，但边界没处理、错误被吞、测试写的是"能过"而不是"该过"。所以逐行读实现的性价比下降，review 重心要移到需求和边界上——它解决的是不是对的问题；
		官方 best practice 里我认为最值钱的一条是"给 AI 一个它能自己跑的验证"（tests/build/lint/截图），没有验证回路，"looks done"就是它唯一的停止信号，你就变成了人肉 CI。TDD 在 AI 时代被重新定价：测试从"锦上添花"变成控制 AI 的主要手段——你不是在 review 代码，是在 review 验收标准；
		我的习惯：先让 AI 写测试、人确认测试，再让 AI 实现；另外重点盯 AI 顺手改的公共代码、并发时序、安全和权限默认值；踩过的坑沉淀回规则文件，让同类错误不出现第二次。

- 团队推 AI 提效，你怎么设计和衡量？说说你对 vibe coding 边界的判断。

		vibe coding（Karpathy 提出的说法）：全托付式让 AI 写，人不看 diff。适合：原型验证、一次性脚本、demo——判断标准就一条"错了谁能兜底、兜底成本多高"，兜底成本低于重写成本就可以 vibe；生产系统不行，因为它积累的是看不见的债，出事故时没有任何人能定位；
		团队衡量，我不看"AI 生成代码占比"这种容易造假的数字，看质量信号（缺陷逃逸率、review 打回率、revert 率）+ 产出信号（需求前置时间、merge 周期）+ 使用深度（高频场景渗透：脚手架/测试/迁移/文档）。缺陷逃逸率是最硬的指标；
		还要防指标变 KPI 的副作用——有人拿 AI 刷生成量，所以 review 环节必须有人认这条规则：产出多少不看，看删了多少、担了多少责。

- 换模型/换供应商（跨模型工作），web 侧怎么设计抽象层？哪些差异是前端要显式处理的？

		接口形状其实各家都收敛到 OpenAI-compatible 了，真正的差异在行为：流式事件格式不同（增量 piece vs 整块）、工具调用参数流式拼接方式不同、"思考过程"要不要单独通道、上下文窗口大小直接影响你截断/分页策略、结构化输出和 JSON mode 的支持度不一；
		我的设计：薄 provider adapter + 显式 capability 声明（工具调用/思考流/结构化输出/最大上下文），前端只消费自己定义的统一事件模型（这就回到前面 AG-UI 那题——事件协议是比 API 形状更稳定的抽象层）；
		别做的事：把供应商对象直接透传到组件里，那等于把 20 处调用点焊死在一家上。Staff 面这题听的是抽象边界感，不是名词。

- AI 产品的流式响应，web 侧为什么大多用 SSE 而不是 WebSocket？fetch + ReadableStream 怎么实现？为什么不用原生 EventSource？

		先说 EventSource 为什么出局：原生实现只支持 GET、不能带自定义请求头（Authorization 没法放）、不支持 POST body——对话场景请求体必然大，所以实际方案都是 fetch 发请求 + ReadableStream 手动解析 SSE 文本格式；
		为什么不用 WebSocket：LLM 响应是单向推送，SSE 跑在 HTTP 上，网关/代理/鉴权/HTTP/2 多路复用全都复用现成基础设施，还自带浏览器重连语义（虽然要自己补 last-event-id）；真正的增量需求（协作、双向信令）才值得上 WS；
		实现细节：decoder + 按双换行切帧 + 处理半截 chunk（一个 data: 行可能被网络层切开）；中止要用 AbortController 通知后端停止生成（不中止白烧 token）；这题我面过候选人，能说到"半截帧怎么切"的就是真写过。

- 流式输出打字机效果，长列表 + 自动滚动 + 高频更新，前端性能有哪些坑？

		卡顿根因：SSE chunk 到达频率远高于渲染帧率，每个 chunk 一次 setState 就是重渲染风暴。处理是 rAF 合并更新或缓冲区定时 flush，渲染频率和到达频率解耦；
		长列表：已完成的历史消息必须 memo 隔离，只有最后一条在动；列表容器定高 + overflow anchor，否则内容增长会推着视口抖；
		自动滚动要尊重用户意图：用户上翻就停止跟随并出"回到底部"按钮，别抢滚轮；还有一个隐蔽点——流式期间频繁 DOM 变动会拉高 INP，交互埋点和性能监控要区分"流式渲染"这个特殊态（详见后面性能题）。Markdown 增量渲染的坑单独在下题讲。

- AI 回答的 Markdown 是边生成边到达的，增量渲染有哪些坑？代码块、表格在"半截"状态怎么处理？

		核心矛盾：markdown 语法有"未闭合态"——代码块 ``` 没等到配对、表格只到一半、链接 [text](url 被掐断，直接 parse 会渲染错乱或整段闪变；
		方案两条：渲染器容错（streamdown 这类，检测到未闭合语法自动补临时闭合再渲染，内容到达后无缝替换）；或协议侧分段（模型按 block 输出完成标记，前端整块渲染，牺牲一点实时性换稳定）。生产上我倾向分段 + 块内流式混合：正文实时流、代码块整块上；
		还有两个细节：代码高亮别每个 token 全量重 highlight（增量高亮或防抖）；渲染 AI 生成的 HTML 必须 sanitize（见安全题）。

- 工具调用过程、思考链（reasoning）要在界面上展示，和模型的输出协议怎么设计？说说 AG-UI 这类事件协议解决什么。

		把 agent 行为抽象成事件流，前端是事件状态机不是消息列表。AG-UI（CopilotKit 团队提出的开放协议）的事件族：RunStarted/RunFinished/RunError 管一次运行，TextMessageStart/Content/End 流式文本，ToolCallStart/Args/End/Result 流式工具调用（参数本身就是流式拼接的，可以实时渲染"正在调什么"），StateSnapshot/StateDelta 做共享状态同步（snapshot 初始化 + JSON Patch 增量），MessagesSnapshot 断线对账，还有 Reasoning 事件族单独走思考流；
		它解决的正是我前面那题说的：事件协议比 API 形状更稳定，换 agent 框架不用重写前端；interrupt 机制（RunFinished 带 outcome: interrupt）把"暂停等人确认再续跑"标准化了，人机确认不用各家自造；
		前端渲染价值排序：工具调用 > 思考链 > 原始日志，用户要的是"它在干什么"的进度感，不是把 debug 面板给用户看——这个取舍本身就是好的面试得分点。

- 生成式 UI（generative UI）是什么？让模型"输出组件"怎么落地？有哪些坑？

		本质是把模型的 tool call 直接映射成组件：Vercel AI SDK 的 streamUI（RSC 方案）让工具返回 React 组件、服务端流给客户端，模型相当于一个"动态路由器"——理解意图后决定渲染哪个组件；工具里用 async generator，先 yield Loading 再 return 结果组件；
		坑：一是官方自己标注 experimental、建议生产走 AI SDK UI（工具返回数据、客户端映射渲染），照搬教程上生产就是给自己埋雷；二是安全边界——能渲染的组件必须是白名单预注册的，模型只出"选择题"不出"填空题"，否则就是远程代码执行；三是流式组件的"完成态对账"——中途刷新/断线后半成品组件怎么恢复，要配合消息持久化；
		价值判断：表单/卡片/图表这类结构固定的场景收益大；别为了炫技让模型生成整页布局，那是不确定输出放大 UI 不一致。

- 流式回答未完成用户就刷新了/断网重连了，消息怎么幂等、状态怎么恢复？

		三层设计：消息 ID 服务端分配（客户端临时 id 必须可对账替换），重试携带幂等键，杜绝"同一条消息出现两次"；恢复靠快照 + 增量：重连先拉 MessagesSnapshot/完整消息列表，再接续 delta，别假设客户端缓存可信；
		流中断的"半成品"怎么处理要定策略：常见是落库时带 incomplete 标记，重连后要么从断点续传（服务端要持久化生成中间态，工程量大），要么明确作废重新生成并把已生成部分作为上下文；两者都行，但必须有其一，"看情况"就是没想过；
		可观测配套：SSE 断流率、重连恢复成功率要上报——流式产品的这条监控和 CRUD 产品的接口成功率同等重要。

- AI 对话产品的性能指标和传统 Web 有什么不同？TTFT、token 成本这些怎么纳入前端视野？

		指标体系变了：传统看 LCP/INP/CLS，AI 产品第一指标是 TTFT（首 token 时间，对应体感"开始响应没"）和 token 间间隔（决定"流得顺不顺"），这两个才是流式产品的"性能预算"；CWV 依然要盯——尤其流式渲染频繁变动拉高的 CLS 和 INP，两个体系并存；
		长回复失败重来的代价极大（时间和 token 双成本），所以前端要有"中断/重试/续传"的产品化设计（上一题的协议是底座）；成本进前端视野：不同模型档位（haiku/sonnet 类 routing 思路）的延迟和价格差异是用户体验的一部分，简单任务路由到小模型是"体验成本三角"的常规解；
		还有质量指标：拒答率、人工接管率、答案反馈率——前端是这些信号唯一的采集现场，这题答到这里就是产品型选手的信号。

- 会话消息状态在前端怎么管理？以什么为真相源？乐观更新和中断、重新生成这些操作怎么设计？

		真相源必须在服务端（持久化的会话记录），前端的 pending/streaming/complete 只是渲染状态机，刷新后一切以服务端对账——这个定位说不清，后面的设计全是漏的；
		操作设计：发送乐观插入（临时 id + 失败回滚）；中断 = AbortController 掐流 + 通知服务端停生成 + 本地定稿为"已中断"态（要落库，刷新后还在）；重新生成分两种语义——同消息新版本（服务端 version 链，UI 可切换）或新消息替换（简单但历史丢失），选型看产品定位；编辑重发等于截断历史重开分支；
		隐藏考点是多标签页/多端一致：同一会话两个 tab 同时发消息怎么办（乐观锁 or 版本号冲突提示），能主动讲到这层的候选人不多。

- AI 生成内容（Markdown/HTML/链接/代码）渲染到页面上，XSS 和 prompt injection 怎么防？

		AI 生成内容要当"用户输入"的同级对待——它本来就源自用户输入 + 不可控的模型行为，sanitize 一步不能少：Markdown 渲染禁 raw HTML 或严格白名单（DOMPurify 兜底）、链接 href 协议白名单（javascript: 直接杀）、代码块只高亮不执行；
		AI 场景特有两条：一是 AI 生成的链接带域名提示和风险提示——用户因为"信任 AI"而降低警惕，这是信任转移攻击，安全产品意识在这题里；二是 prompt injection 的源头是模型读到的外部内容（网页/文档里藏指令），前端根治不了，但要限制影响面：注入指令最终往往落在敏感操作上，所以敏感操作强制人确认（见 HITL 题），并把"这段内容来自外部"渲染出来（来源标注即安全设计）；
		 CSP 该上上（script-src 收紧、禁用 unsafe-eval 的场景注意高亮库），把责任边界说清楚：前端不承诺防注入，前端承诺的是不给注入放大杀伤面的机会。

- AI 功能上线后，怎么做可观测性和质量监控？这道题只答接口日志就偏表面，往深挖。

		分三层：技术层（错误率、延迟分位、TTFT、token 消耗、流中断率）；行为层（中断率、重新生成率、复制率、停留时长——这些是"答案质量"的代理指标，前端埋点的主场）；质量层（赞踩反馈、抽样人评、离线 eval 集回归）；
		关键设计是一条 trace id 贯穿：前端请求 id -> 网关 -> 模型调用 -> 工具调用链，否则线上"这个回答很蠢"根本无从复盘；换模型/改 prompt 要像发版一样先跑 eval 集回归——评测接 CI 是 AI 团队的成熟度分水岭；
		别只报监控数字，补一句"哪些信号该触发回滚/降级"（比如踩率超阈值自动切回上一版 prompt），闭环才算完整。

- 哪些 AI 功能必须 human in the loop（人来确认），哪些可以全自动？这个边界怎么定？

		我的判据是错误成本的可逆性：不可逆或影响真实世界的操作必须确认——下单、支付、删除、发消息给别人、改数据、执行命令；纯信息加工类（摘要、问答、草稿生成）可以自动，因为错了代价只是重来一次；
		确认 UI 的讲究：把"将要执行的具体动作和数据"摆出来（金额、收件人、diff），而不是一个"是否继续？"——没有信息的确认等于白点；协议上 AG-UI 的 interrupt（RunFinished 带 interrupts 数组、前端收集 answer 后 resume）就是这个模式的标准化，说明行业已经收敛；
		最高分的答法是承认灰度：权限分级（读操作自动、写操作确认、危险操作双重确认），类比 Claude Code 的 permission 模型——这题本质在考古你的风险判断力，不是技术名词。

- 做一个知识库问答（RAG）产品的前端，有哪些比"接个聊天框"深的点？

		来源是一等公民：引用角标（点击滚动定位到来源卡片）、原文高亮片段（chunk 级定位）、"生成文本 vs 引用片段"的视觉区分、来源可用性兜底（原文已删/无权限）——这些是产品可信度的地基，不是装饰；
		幻觉监控前端能做一件事：校验引用完整性——模型标注的引用 id 必须都在返回的 chunks 里，"无来源的断言"标灰并计数，这本身就是质量信号，接到上面的可观测体系里；
		延迟结构：RAG 的链路是 检索->重排->生成，检索耗时可先展示"找到 N 篇资料"再流式生成，分段进度比整体转圈体感好得多；追问的上下文窗口管理（多轮里检索 query 要不要重写）也要和后端约定清楚边界。

- 让 AI 生成整块 UI 时，怎么防止它产出一堆"能跑但不像我们的产品"的代码？

		根因是模型不知道你的"默认审美和约束"，只会写互联网平均值。对策分三层：把设计系统喂进上下文（DESIGN.md / 组件清单 / token，或把组件库文档做成 MCP/skill 让它按需查），AI 只会用你有的组件才拼得出你的界面；		约束产出形态：规则文件里写死"不许自造 card/panel CSS、必须用 X 组件库、样式走 token 不写死色值、布局用 Grid/flex 不用绝对定位堆"，配 stylelint/ESLint 把违反项在 CI 挡住，光靠提示词管不住；		最后一公里：给视觉验证回路——生成后截图对比设计稿、列出差异再改（官方 best practice 的 verify 思路），没有这层就退化成"看起来完成了"。我的经验是先花一天把"我们的前端规矩"写成规则文件，后面 AI 质量直接抬一档。

- Prompt / 上下文 / 工具定义这些"AI 侧的资产"，怎么做版本管理和回归？它算不算代码？

		我的立场：算，而且要当代码治理。prompt、system message、工具 schema、CLAUDE.md/AGENTS.md 都是"影响模型行为的源"，改动等于改逻辑，必须进 Git、走 review、能 diff 能回滚；散落在各处、只有某人知道的那个 prompt 就是定时炸弹；		回归靠 eval 集：把典型输入 + 期望行为固化成用例，改 prompt/换模型前后跑一遍，接进 CI 当门禁（哪怕先用规则 + 少量 LLM-as-judge 打分，也别纯靠"我感觉这次回答更好"）；		工具定义尤其要管：改一个工具的 description/参数，可能悄悄改变模型调用它的时机，这属于"看起来没动代码却动了行为"的高危变更，必须带 case 验证；把 prompt 版本和模型版本一起记录，线上问题才能复现到具体组合。

- MCP 对前端意味着什么？为什么说它可能重演"接口标准化"？

		MCP（Model Context Protocol）把"模型如何连接外部工具和数据源"标准化成 client-server 协议，工具/资源/prompt 三类能力用统一 schema 暴露。对前端的直接意义：过去每个 AI 应用都要手写一堆胶水去接数据库、文件系统、内部 API，现在这些能力可复用、可插拔，前端能像调 REST 一样调"能力"；		类比接口标准化很到位：在 MCP 之前，每对 agent-tool 集成都是定制 N×M，有了它变成 N+M（工具写一次 server、被任意宿主调用），这就是协议收敛的价值——和当年 OpenAPI 让前后端契约标准化同构；		但保持清醒：MCP 也带来新的攻击面（第三方 server 的 prompt injection、工具描述本身可被投毒），选第三方 MCP 要像选 npm 依赖一样看来源、限权限；前端在 UI 里要把"这个操作会调用哪个外部能力"显性化，别让模型静默越权。

- AI 产品的成本怎么控？除了"少调用"，前端在成本优化里具体能做什么？

		成本大头是 token（输入 + 输出）和调用次数，输入侧最容易被忽视——超长上下文、每轮都重传历史、system prompt 里塞满用不上的东西，都在悄悄烧钱。前端能做的：会话历史做滑窗/摘要（呼应上下文工程的 compaction）、按需检索只带高信号片段、别把整篇文档原文重复贴进每轮请求；		模型路由：简单任务走小模型、复杂再升档（routing 模式），前端可以按意图/内容长度决定调哪个模型档位，这是体验成本三角的常规解；缓存：语义相近或相同请求做结果缓存、RAG 检索层缓存；流式提前中断（用户点了停止就 AbortController 通知后端别再产出，省输出 token）；		把成本做成可观测指标：每功能/每用户的 token 消耗上报，才能定位"哪个交互在漏钱"——只会说"少调用"是没上过线。

- 面向 C 端的 AI 功能，产品形态上 2026 年有哪些被验证过的模式？

		聊天不是唯一形态，甚至对多数 C 端不是最优——纯对话框把"用户要会提问"的成本甩给了用户。被验证的模式：嵌入式辅助（在用户干原任务的现场给建议，写作工具的行内改写、IDE 的代码补全、表单的智能填充），零学习成本、上下文天然对齐；		草稿 + 人工确认（AI 生成初稿、用户改定），把"不可信的模型输出"降级成"可编辑的建议"，规避幻觉责任问题；结构化生成（让模型填模板/卡片而非自由长文，配合生成式 UI），比大段文字更可控；渐进暴露（默认简单，重度用户才展开高级能力）；		我的判断：好形态的标准是"用户不需要理解 AI 也能获益"——先想清楚这个功能是提效还是创造，提效走嵌入式，创造才值得开一个对话面板，别无脑套聊天框。

- 基模越来越强，作为工程师你的优势是什么？（2026 AI 编程高频题）

		这题先排雷：答"AI 做不了复杂业务、安全代码、并发"已经过时了，2026 年这些 AI 都写得有模有样，面试官一句"你给够上下文了吗"就能反问倒；防守型答案越守越窄；
		正解是换框架：AI 的输出质量取决于人的输入质量——问题定义（把"加个退款"拆成部分退款、幂等、超时关闭这些边界）、上下文构建（该给什么不该给什么）、结果验证（验证业务语义而不是"能不能跑通"）、技术决策（团队现状和历史包袱 AI 不知道）、成本控制（什么活配什么模型），这五件事是 AI 时代人的杠杆；
		收尾用一句定性："我的优势不是比 AI 写得好，是让 AI 写得更好"；这是驱动型答案——只要 AI 还需要人驱动，优势就在；能现场用一个自己项目的例子把五个能力套进去的，这题就是满分；

- 你负责的模块里，哪些代码让 AI 写、哪些自己写？判断标准是什么？（2026 AI 编程面经）

		判断标准不是"AI 能不能写"（都能写），是两条轴：出 bug 的代价大小 × 让 AI 写的综合成本（组织上下文 + 审查 + 返工）；
		代价小、AI 更省时的放心交出去：CRUD、样板、胶水代码、测试用例、一次性脚本、不熟语言的初版实现；代价大的严格审查或自己写：资金和权限语义、并发与状态机、性能敏感路径、以及你自己不熟的领域——你审不动的代码不该由 AI 代写上线；
		还有一类要反着说：你已经定位清楚的小修改别丢给 AI——报错知道在哪一行、加个判空十秒的事，交给 AI 要它读文件、分析、生成、你再审查，几万 token 换回一个更慢更贵的十分钟；答得出"哪些场景我拒绝用 AI"，比只会喊提效的人真实得多；

- AI 生成的"合理但错误"的代码有什么特征？review 时怎么防？（2026 AI 编程面经）

		特征是"逻辑通顺、能跑、命名工整，但业务语义偏了"：退款退错对象、权限用了错误的角色、金额精度悄悄丢两位小数；它比普通 bug 更危险，因为"看起来太对了"，是最容易穿过 Code Review 的一类；
		防法三层：审查重点从语法挪到业务语义（对着需求核金额、对象、幂等、边界，不是逐行看写法）；测试先行（让 AI 先把验收条件写成测试，再用实现去绿它——测试即规格，人至少锁死了规格）；核心路径人工重写或结对确认；
		和人写的代码的本质差异：人错在"不会或疏漏"，AI 错在"自信地编造"——编不存在的 API、配置项、业务规则；所以 review 清单要换一条：这个接口/字段/配置真实存在吗？这条规则我什么时候告诉过它？两个问题问完，一半的幻觉就现形了；

- AI 生成的代码出了线上 bug，你的处理流程是什么？（2026 AI 编程面经）

		三步走，顺序不能乱：先止血（回滚或降级——不管代码是不是 AI 写的，线上处置标准一致）；再定因（监控定影响面，日志链路定位到代码行）；最后补流程（回答"review 为什么没拦住"）；
		定因时要分层归责，结论完全不同：是上下文缺失（业务规则从没喂给它）、验证不足（测试没覆盖这个边界）、还是审查失守（accept 的人没真读懂）——分别对应"补规则文件、补测试、改审查流程"三种补丁；
		一个 bug 不可怕，同类再出才可怕：把结论沉淀成"哪些模块允许 AI 生成、允许到什么深度"的准入清单；面试里能把事故讲成流程改进的闭环，比讲技术细节更打动面试官；

- AI 写的代码出了问题，让 AI 自己修也修不好，怎么兜底？（2026 AI 编程面经）

		这场景真实存在：AI 修不好，通常是缺线上感知（它看不到日志监控）或根因跨模块（超它的上下文窗口）；兜底姿势只有一个——人能接手：先回滚止血，自己看日志和链路追踪定位根因，改代码走正常发布；
		能不能接手，取决于当初 review 有没有攒下理解：认真读懂逻辑的 AI 代码，排查起来就是自己的代码；"看着没问题就过"的，和读陌生人代码没区别；这就是"用了 AI 也必须看得懂代码"最硬的理由，也是能力退化的真实代价；
		复盘再定边界：是上下文不够（规则没沉淀进 CLAUDE.md / 仓库文档）还是问题本身超出委托范围，结论决定这类改动下次还交不交给 AI；

- 团队用 AI 编程，Token 成本怎么控制？（2026 AI 编程面经）

		五个策略成套答：模型路由（约七成日常任务小模型够用，大模型输出单价接近小模型二十倍）、上下文按需给（只开相关模块，整仓库塞进去消耗差三五倍，无关代码还会干扰生成质量）、Prompt 一次说清（一轮精确对话 vs 四五轮模糊来回，Token 差几十倍）、缓存复用（Prompt Caching 吃同前缀命中，CRUD 模板让 AI 只填差异）、任务准入（该人写的别给 AI）；
		成本和质量必须一起考核：只砍成本会砍到质量（小模型硬上复杂重构，返工更贵），要看"Token 账单 + AI 代码返工率"两条曲线做平衡；
		注意这题和"AI 产品的推理成本"是两道题：这题是团队编程成本（人和工具），产品调用模型的成本（缓存、降级、限流）另一题会问，答串了说明没审题；

- 用 AI 编程工具，怎么保证不泄露公司代码？（2026 AI 编程面经）

		先承认机制：AI 编程工具都存在代码上行推理的行为，厂商"不用于训练"的承诺和合规审计是两回事，敏感代码不能赌条款；
		工程管控四件套：敏感项目隔离（核心算法、密钥管理、交易策略不进任何外部模型，连复制粘贴问答都不行）、企业版协议（数据隔离和不训练条款）、.claudeignore / .cursorignore 排除敏感目录 + 工具白名单写进团队规范、使用审计留痕；
		前端容易漏的另一面是"进去又出来"：AI 生成代码里硬编码密钥和测试 token、内部接口域名写进组件、把业务敏感字段传给外部 SDK——review 清单要加一条"这段代码有没有暴露内部信息"，仓库侧密钥扫描（gitleaks 类）做最后防线；

- Agent Skills 是什么？和写一段长 Prompt 有什么本质区别？（2026 AI 编程面经）

		Skill 是把"能力"沉淀成可复用、可组合、可被调用的模块——一份 SKILL.md 加脚本资源，按需渐进加载；本质区别：长 Prompt 是每次手搓、质量随人波动、团队没法共享，Skill 是流程资产，一次定义全员调用；
		三个价值：复用性（同流程不用重写）、一致性（新人调 code-review skill 就能产出团队标准的审查结论，Skill 成了"隐性规范的载体"）、上下文经济性（Skill 按需加载，长 Prompt 每轮常驻烧 token）；
		追问一般是"它和 MCP、sub-agent 的边界"：Skill 管流程和知识（怎么做的沉淀），MCP 管工具接入（用什么做），sub-agent 管上下文隔离（在哪做、谁来做）；三者组合才是完整的 Agent 工程栈；

- 用 AI IDE（Cursor 一类）长期做大项目，你总结出哪些方法论？（2026 AI 编程面经）

		方法论四条实在的：先让 AI 学项目再接任务（大项目先让它通读代码库产出架构和模块职责文档，人和 AI 对齐理解再动手，这一步决定后续协作质量）；一个会话只做一件事（新任务开新 chat，防历史对话污染上下文）；定期删废弃代码（仓库里的冗余实现会持续误导 AI，越拖越差）；落地后让 AI 复盘抽指南（把实现过程沉淀成操作指南，类似需求直接复用）；
		配置层的两件事：规则文件（.cursorrules / CLAUDE.md）定义生成风格和禁区，ignore 文件划访问边界——"AI 改坏东西"很多时候是边界没配好；
		还有一条反直觉的：越用 AI 越考验拆任务的能力——需求要拆到"一次会话可完成、可独立验证"的粒度；判断 AI 产出变差的顺序也是内行的：先查上下文质量，再查任务粒度，最后才考虑换模型；

- Claude Code 为什么不用 RAG 检索代码，而是用 grep/glob/read 的 agentic search？（2026 AI 编程面经）

		Anthropic 的工程实践给过答案：代码是高结构、可精确检索的文本——符号名、import 链、目录约定本身就是天然索引，grep 的精确命中加模型的多轮判断，比向量相似度稳；embedding 检索在代码上经常召回"形似神不似"的片段，反而污染上下文；
		更关键的是检索姿势：agentic search 是"边查边想"——先看目录、再 grep、只读命中的片段，按需拉取天然控制上下文体积；RAG 是一次性召回一堆，token 花在噪声上，还有注意力稀释问题；工具循环的成本被模型调用开销掩盖后，效果反而更好；
		高分答法是留边界不站队：海量代码加固定问题模式（全库安全扫描、跨仓规范问答）里 embedding 粗筛加 grep 精定位的混合方案仍然有价值；这题考的是"检索策略要匹配数据结构和查询模式"的判断力，不是选阵营；

- 拆解一下 Claude Code 的核心工作循环（agent loop）？auto-compact 是怎么回事？（2026 AI 编程面经）

		循环本质：任务 + 工具定义 + 对话历史发给模型 → 模型要么给答案、要么发起工具调用（读文件、编辑、执行命令）→ 工具结果回填上下文 → 再问模型，直到不再调工具；看起来就是一个 while，工程全在外围：权限审批（哪些命令要人点头）、失败重试、任务清单（todo 工具是模型和外层共享状态的通道）；
		上下文管理是命门：窗口快满时 auto-compact——前段对话被摘要重写，保留关键决策、文件路径、未完成任务，牺牲细节换继续跑的能力；所以长任务要靠外置记忆：重要结论写进文件和任务清单，光指望对话记住的东西会被压缩掉；
		最底层的一句话：模型是状态无感的，所有"持续性"都来自循环外围的工程——文件系统、git、CLAUDE.md、任务清单；把 harness 这层讲清楚，就证明了你知道"智能"和"产品"之间差的是什么；

- 什么是 Spec-Driven Development？vibe coding 为什么在交付场景要走向规格、计划、任务、验证？（2026 AI 编程面经）

		定义：先产出可审查的规格（要什么、边界、验收标准），再从 spec 派生计划、拆任务、实现与验证对齐——文档从"人看的附属品"变成"人和 AI 对齐的主工件"；
		动因很实在：AI 产出质量的上限就是输入规格的质量，一句话需求必然产出"看起来像那么回事"的东西；vibe 模式（不审查直接 accept）适合原型和一次性玩具，进不了有存量约束、有质量要求的产品工程；
		生态位了解几个名字即可（OpenSpec、Spec Kit 这类把 spec→plan→tasks 文件化的工具）；和 CLAUDE.md 的分工要说得清：规则文件管"长期约束和风格"，spec 管"单个需求的完整定义"，一个像团队公约，一个像合同；

- vibe coding 在 Git 检查点、数据库变更、线上回滚上有哪些翻车点，怎么防？（2026 AI 编程面经）

		AI 没有后悔药，工程后悔药得提前埋：动手前工作区保持干净（可回滚的检查点），大改开分支，小步提交——每步可编译可回退；一次让 AI 改十几个文件还不验证，是最典型的翻车姿势；
		数据和环境单独防：破坏性迁移、删表、批量 update 之前必须备份（AI 执行 SQL 不看场合）；密钥既不进对话也不进生成代码，仓库侧加密钥扫描兜底；线上侧照旧：灰度、回滚预案一个不能少，工具变了发布纪律不能变；
		这题面试官在等的态度是"你能不能对 AI 的产出负责"：accept 的每行代码你都要能背下来，出事你都要能接手——把责任归属讲明白，比讲任何工具技巧都加分；

- AI 会淘汰初级程序员吗？初级在 AI 时代该建什么能力结构？（2026 高频开放题）

		别答"会/不会"二选一：AI 消灭的是"以翻译需求为生的编码工位"，不是消灭初级——但初级的价值锚点已经从"能写完"迁移到"能定义清楚、能验证正确、能理解系统"；
		能力结构给四条：需求拆解（一句话变规格）、代码理解力（读得懂比写得快值钱——AI 时代理解力就是兜底力）、系统观（知道自己模块在整体链路里的位置）、AI 协作（上下文管理、判断产出质量、工具链配置）；
		表态也要给：日常在用 AI、有自己的方法论、但对产出保持审查和不信任默认值——"用而不盲信"六个字是这题的题眼；企业视角补一句就完整：纯编码岗在缩，"会用 AI 快速交付业务价值"的岗在涨，这恰好是初级的新入场券；

## <a name='other'>其他问题</a>

- 原来公司工作流程是怎么样的，如何与其他人协作的？如何跨部门合作的？

- 你遇到过比较难的技术问题是？你是如何解决的？

- 设计模式 知道什么是singleton, factory, strategy, decrator么?

- 常使用的库有哪些？常用的前端开发工具？开发过什么应用或组件？

- 页面重构怎么操作？

		网站重构：在不改变外部行为的前提下，简化结构、添加可读性，而在网站前端保持一致的行为。
		也就是说是在不改变UI的情况下，对网站进行优化，在扩展的同时保持一致的UI。

		对于传统的网站来说重构通常是：

		表格(table)布局改为DIV+CSS
		使网站前端兼容于现代浏览器(针对于不合规范的CSS、如对IE6有效的)
		对于移动平台的优化
		针对于SEO进行优化
		深层次的网站重构应该考虑的方面

		减少代码间的耦合
		让代码保持弹性
		严格按规范编写代码
		设计可扩展的API
		代替旧有的框架、语言(如VB)
		增强用户体验
		通常来说对于速度的优化也包含在重构中

		压缩JS、CSS、image等前端资源(通常是由服务器来解决)
		程序的性能优化(如数据读写)
		采用CDN来加速资源加载
		对于JS DOM的优化
		HTTP服务器的文件缓存

- 列举IE与其他浏览器不一样的特性？


		1、事件不同之处：

		   	触发事件的元素被认为是目标（target）。而在 IE 中，目标包含在 event 对象的 srcElement 属性；

			获取字符代码、如果按键代表一个字符（shift、ctrl、alt除外），IE 的 keyCode 会返回字符代码（Unicode），DOM 中按键的代码和字符是分离的，要获取字符代码，需要使用 charCode 属性；

			阻止某个事件的默认行为，IE 中阻止某个事件的默认行为，必须将 returnValue 属性设置为 false，Mozilla 中，需要调用 preventDefault() 方法；

			停止事件冒泡，IE 中阻止事件进一步冒泡，需要设置 cancelBubble 为 true，Mozzilla 中，需要调用 stopPropagation()；


- 什么叫优雅降级和渐进增强？

		优雅降级：Web站点在所有新式浏览器中都能正常工作，如果用户使用的是老式浏览器，则代码会针对旧版本的IE进行降级处理了,使之在旧式浏览器上以某种形式降级体验却不至于完全不能用。
		如：border-shadow

		渐进增强：从被所有浏览器支持的基本功能开始，逐步地添加那些只有新版本浏览器才支持的功能,向页面增加不影响基础浏览器的额外样式和功能的。当浏览器支持时，它们会自动地呈现出来并发挥作用。
		如：默认使用flash上传，但如果浏览器支持 HTML5 的文件上传功能，则使用HTML5实现更好的体验；

- 是否了解公钥加密和私钥加密。

		一般情况下是指私钥用于对数据进行签名，公钥用于对签名进行验证;
		HTTP网站在浏览器端用公钥加密敏感数据，然后在服务器端再用私钥解密。


- WEB应用从服务器主动推送Data到客户端有那些方式？

		html5提供的Websocket
		不可见的iframe
	    WebSocket通过Flash
	    XHR长时间连接
	    XHR Multipart Streaming
	    <script>标签的长时间连接(可跨域)

- 对Node的优点和缺点提出了自己的看法？


		*（优点）因为Node是基于事件驱动和无阻塞的，所以非常适合处理并发请求，
          因此构建在Node上的代理服务器相比其他技术实现（如Ruby）的服务器表现要好得多。
		  此外，与Node代理服务器交互的客户端代码是由javascript语言编写的，
	      因此客户端和服务器端都用同一种语言编写，这是非常美妙的事情。

		*（缺点）Node是一个相对新的开源项目，所以不太稳定，它总是一直在变，
          而且缺少足够多的第三方库支持。看起来，就像是Ruby/Rails当年的样子。


- 你有用过哪些前端性能优化的方法？

		  （1） 减少http请求次数：CSS Sprites, JS、CSS源码压缩、图片大小控制合适；网页Gzip，CDN托管，data缓存 ，图片服务器。

		  （2） 前端模板 JS+数据，减少由于HTML标签导致的带宽浪费，前端用变量保存AJAX请求结果，每次操作本地变量，不用请求，减少请求次数

		  （3） 用innerHTML代替DOM操作，减少DOM操作次数，优化javascript性能。

		  （4） 当需要设置的样式很多时设置className而不是直接操作style。

		  （5） 少用全局变量、缓存DOM节点查找的结果。减少IO读取操作。

		  （6） 避免使用CSS Expression（css表达式)又称Dynamic properties(动态属性)。

		  （7） 图片预加载，将样式表放在顶部，将脚本放在底部  加上时间戳。

		  （8） 避免在页面的主体布局中使用table，table要等其中的内容完全下载之后才会显示出来，显示比div+css布局慢。
		  对普通的网站有一个统一的思路，就是尽量向前端优化、减少数据库操作、减少磁盘IO。向前端优化指的是，在不影响功能和体验的情况下，能在浏览器执行的不要在服务端执行，能在缓存服务器上直接返回的不要到应用服务器，程序能直接取得的结果不要到外部取得，本机内能取得的数据不要到远程取，内存能取到的不要到磁盘取，缓存中有的不要去数据库查询。减少数据库操作指减少更新次数、缓存结果减少查询次数、将数据库执行的操作尽可能的让你的程序完成（例如join查询），减少磁盘IO指尽量不使用文件系统作为缓存、减少读写文件次数等。程序优化永远要优化慢的部分，换语言是无法“优化”的。

- http状态码有那些？分别代表是什么意思？

			简单版
			[
				100  Continue	继续，一般在发送post请求时，已发送了http header之后服务端将返回此信息，表示确认，之后发送具体参数信息
				200  OK 		正常返回信息
				201  Created  	请求成功并且服务器创建了新的资源
				202  Accepted 	服务器已接受请求，但尚未处理
				301  Moved Permanently  请求的网页已永久移动到新位置。
				302 Found  		临时性重定向。
				303 See Other  	临时性重定向，且总是使用 GET 请求新的 URI。
				304  Not Modified 自从上次请求后，请求的网页未修改过。

				400 Bad Request  服务器无法理解请求的格式，客户端不应当尝试再次使用相同的内容发起请求。
				401 Unauthorized 请求未授权。
				403 Forbidden  	禁止访问。
				404 Not Found  	找不到如何与 URI 相匹配的资源。

				500 Internal Server Error  最常见的服务器端错误。
				503 Service Unavailable 服务器端暂时无法处理请求（可能是过载或维护）。
			]

		  完整版
		  1**(信息类)：表示接收到请求并且继续处理
			100——客户必须继续发出请求
			101——客户要求服务器根据请求转换HTTP协议版本

		  2**(响应成功)：表示动作被成功接收、理解和接受
			200——表明该请求被成功地完成，所请求的资源发送回客户端
			201——提示知道新文件的URL
			202——接受和处理、但处理未完成
			203——返回信息不确定或不完整
			204——请求收到，但返回信息为空
			205——服务器完成了请求，用户代理必须复位当前已经浏览过的文件
			206——服务器已经完成了部分用户的GET请求

		  3**(重定向类)：为了完成指定的动作，必须接受进一步处理
			300——请求的资源可在多处得到
			301——本网页被永久性转移到另一个URL
			302——请求的网页被转移到一个新的地址，但客户访问仍继续通过原始URL地址，重定向，新的URL会在response中的Location中返回，浏览器将会使用新的URL发出新的Request。
			303——建议客户访问其他URL或访问方式
			304——自从上次请求后，请求的网页未修改过，服务器返回此响应时，不会返回网页内容，代表上次的文档已经被缓存了，还可以继续使用
			305——请求的资源必须从服务器指定的地址得到
			306——前一版本HTTP中使用的代码，现行版本中不再使用
			307——申明请求的资源临时性删除

		  4**(客户端错误类)：请求包含错误语法或不能正确执行
			400——客户端请求有语法错误，不能被服务器所理解
			401——请求未经授权，这个状态代码必须和WWW-Authenticate报头域一起使用
			HTTP 401.1 - 未授权：登录失败
			　　HTTP 401.2 - 未授权：服务器配置问题导致登录失败
			　　HTTP 401.3 - ACL 禁止访问资源
			　　HTTP 401.4 - 未授权：授权被筛选器拒绝
			HTTP 401.5 - 未授权：ISAPI 或 CGI 授权失败
			402——保留有效ChargeTo头响应
			403——禁止访问，服务器收到请求，但是拒绝提供服务
			HTTP 403.1 禁止访问：禁止可执行访问
			　　HTTP 403.2 - 禁止访问：禁止读访问
			　　HTTP 403.3 - 禁止访问：禁止写访问
			　　HTTP 403.4 - 禁止访问：要求 SSL
			　　HTTP 403.5 - 禁止访问：要求 SSL 128
			　　HTTP 403.6 - 禁止访问：IP 地址被拒绝
			　　HTTP 403.7 - 禁止访问：要求客户证书
			　　HTTP 403.8 - 禁止访问：禁止站点访问
			　　HTTP 403.9 - 禁止访问：连接的用户过多
			　　HTTP 403.10 - 禁止访问：配置无效
			　　HTTP 403.11 - 禁止访问：密码更改
			　　HTTP 403.12 - 禁止访问：映射器拒绝访问
			　　HTTP 403.13 - 禁止访问：客户证书已被吊销
			　　HTTP 403.15 - 禁止访问：客户访问许可过多
			　　HTTP 403.16 - 禁止访问：客户证书不可信或者无效
			HTTP 403.17 - 禁止访问：客户证书已经到期或者尚未生效
			404——一个404错误表明可连接服务器，但服务器无法取得所请求的网页，请求资源不存在。eg：输入了错误的URL
			405——用户在Request-Line字段定义的方法不允许
			406——根据用户发送的Accept拖，请求资源不可访问
			407——类似401，用户必须首先在代理服务器上得到授权
			408——客户端没有在用户指定的饿时间内完成请求
			409——对当前资源状态，请求不能完成
			410——服务器上不再有此资源且无进一步的参考地址
			411——服务器拒绝用户定义的Content-Length属性请求
			412——一个或多个请求头字段在当前请求中错误
			413——请求的资源大于服务器允许的大小
			414——请求的资源URL长于服务器允许的长度
			415——请求资源不支持请求项目格式
			416——请求中包含Range请求头字段，在当前请求资源范围内没有range指示值，请求也不包含If-Range请求头字段
			417——服务器不满足请求Expect头字段指定的期望值，如果是代理服务器，可能是下一级服务器不能满足请求长。

		  5**(服务端错误类)：服务器不能正确执行一个正确的请求
			HTTP 500 - 服务器遇到错误，无法完成请求
			　　HTTP 500.100 - 内部服务器错误 - ASP 错误
			　　HTTP 500-11 服务器关闭
			　　HTTP 500-12 应用程序重新启动
			　　HTTP 500-13 - 服务器太忙
			　　HTTP 500-14 - 应用程序无效
			　　HTTP 500-15 - 不允许请求 global.asa
			　　Error 501 - 未实现
		  HTTP 502 - 网关错误
		  HTTP 503：由于超载或停机维护，服务器目前无法使用，一段时间后可能恢复正常

- 一个页面从输入 URL 到页面加载显示完成，这个过程中都发生了什么？（流程说的越详细越好）

		  注：这题胜在区分度高，知识点覆盖广，再不懂的人，也能答出几句，
		  而高手可以根据自己擅长的领域自由发挥，从URL规范、HTTP协议、DNS、CDN、数据库查询、
		  到浏览器流式解析、CSS规则构建、layout、paint、onload/domready、JS执行、JS API绑定等等；

		  详细版：
			1、浏览器会开启一个线程来处理这个请求，对 URL 分析判断如果是 http 协议就按照 Web 方式来处理;
			2、调用浏览器内核中的对应方法，比如 WebView 中的 loadUrl 方法;
		    3、通过DNS解析获取网址的IP地址，设置 UA 等信息发出第二个GET请求;
			4、进行HTTP协议会话，客户端发送报头(请求报头);
		    5、进入到web服务器上的 Web Server，如 Apache、Tomcat、Node.JS 等服务器;
		    6、进入部署好的后端应用，如 PHP、Java、JavaScript、Python 等，找到对应的请求处理;
			7、处理结束回馈报头，此处如果浏览器访问过，缓存上有对应资源，会与服务器最后修改时间对比，一致则返回304;
		    8、浏览器开始下载html文档(响应报头，状态码200)，同时使用缓存;
		    9、文档树建立，根据标记请求所需指定MIME类型的文件（比如css、js）,同时设置了cookie;
		    10、页面开始渲染DOM，JS根据DOM API操作DOM,执行事件绑定等，页面显示完成。

		  简洁版：
			浏览器根据请求的URL交给DNS域名解析，找到真实IP，向服务器发起请求；
			服务器交给后台处理完成后返回数据，浏览器接收文件（HTML、JS、CSS、图象等）；
			浏览器对加载到的资源（HTML、JS、CSS等）进行语法解析，建立相应的内部数据结构（如HTML的DOM）；
			载入解析到的资源文件，渲染页面，完成。

- 部分地区用户反应网站很卡，请问有哪些可能性的原因，以及解决方法？

- 从打开app到刷新出内容，整个过程中都发生了什么，如果感觉慢，怎么定位问题，怎么解决?

- 第一次访问页面中时弹出引导，用户关闭引导，之后再次进入页面时不希望出现引导，如何实现？

			localStorage

- 除了前端以外还了解什么其它技术么？你最最厉害的技能是什么？

- 你用的得心应手用的熟练地编辑器&开发环境是什么样子？

		Sublime Text 3 + 插件
		Google chrome 查看页面UI、动画效果和交互功能，Firebug 兼容测试和
		Node.js + webpack
		Git 版本控制和Code Review

- 对前端工程师这个职位是怎么样理解的？它的前景会怎么样？

	    前端是最贴近用户的程序员，比后端、数据库、产品经理、运营、安全都近。
		1、实现界面交互
		2、提升用户体验
		3、有了Node.js，前端可以实现服务端的一些事情


		前端是最贴近用户的程序员，前端的能力就是能让产品从 90分进化到 100 分，甚至更好，

		参与项目，快速高质量完成实现效果图，精确到1px；

		与团队成员，UI设计，产品经理的沟通；

		做好的页面结构，页面重构和用户体验；

		处理hack，兼容、写出优美的代码格式；

		针对服务器的优化、拥抱最新前端技术。

- 你怎么看待Web App 、hybrid App、Native App？

- 你移动端前端开发的理解？（和 Web 前端开发的主要区别是什么？）

- 产品进行版本升级时，可能发生不兼容性问题，如何提前预防和解决？

		非覆盖式发布，API新增而不是在原来的上面修改；
		提前做好 @Deprecated的版本提示；

- 你对加班的看法？


   		加班就像借钱，原则应当是------救急不救穷



- 平时如何管理你的项目？

		先期团队必须确定好全局样式（global.css），编码模式(utf-8) 等；

		编写习惯必须一致（例如都是采用继承式的写法，单样式都写成一行）；

		标注样式编写人，各模块都及时标注（标注关键样式调用的地方）；

		页面进行标注（例如 页面 模块 开始和结束）；

		CSS跟HTML 分文件夹并行存放，命名都得统一（例如style.css）；

		JS 分文件夹存放 命名以该JS功能为准的英文翻译。

		图片采用整合的 images.png png8 格式文件使用 尽量整合在一起使用方便将来的管理

- 如何设计突发大规模并发架构？


- 当团队人手不足，把功能代码写完已经需要加班的情况下，你会做前端代码的测试吗？

- 说说最近最流行的一些东西吧？常去哪些网站？

			ES6\WebAssembly\Node\MVVM\Web Components\React\React Native\Webpack 组件化

- 知道什么是SEO并且怎么优化么? 知道各种meta data的含义么?


- 移动端（Android IOS）怎么做好用户体验?

		清晰的视觉纵线、
		信息的分组、极致的减法、
		利用选择代替输入、
		标签及文字的排布方式、
		依靠明文确认密码、
		合理的键盘利用、

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

		LCP <=2.5s（加载）、INP <=200ms（交互）、CLS <=0.1（视觉稳定性）；
		FID 只测"首次输入"那一次的 input delay（回调开始前的排队时间），覆盖不到后续交互，也解释不了卡顿真正的来源；INP 观测整个会话期间的每一次 click / tap / 键盘交互（不含滚动、悬停），取"最差"的那一次（交互很多时每 50 次忽略 1 个离群值），单次耗时 = input delay（主线程被长任务占着、回调迟迟不开始）+ processing duration（跑事件处理函数）+ presentation delay（处理完到下一帧真正绘制）；
		所以卡顿其实发生在"回调执行 + 下一帧渲染"整段，这正是 FID 测不到的部分（2024-03 正式替换；真实用户按所有页面浏览的 75 分位报告，实验室只能靠 TBT 近似）；
		优化抓手：LCP 看资源优先级/预加载/SSR/CDN；INP 拆长任务、减少 hydration 工作量（RSC/岛架构在这一点上天然加分）；CLS 给图片尺寸占位、字体 fallback 用 size-adjust。

- HTTP/1.1、HTTP/2、HTTP/3 的区别？QUIC 解决了什么问题？0-RTT 是什么？

		1.1：长连接 + 域名分片（6连接限制），有队头阻塞；
		2：二进制分帧、多路复用（解决 HTTP 层队头阻塞）、HPACK 头压缩、服务端推送（实践失败已废）；但 TCP 层丢包仍会卡住所有流；
		3/QUIC：UDP 上的传输层——每条流独立重传（丢包只卡当前流）、0-RTT（会话恢复时首包就带数据，有重放风险）、连接用 ID 标识（换 WiFi/5G 不断线）、把 TLS 握手合并进连接建立省 RTT；
		顺带：移动端弱网收益最大，国内运营商对 UDP 的限速问题也要心里有数。

- HTTPS 握手过程讲一下？为什么是非对称加密 + 对称加密的组合？

		TLS1.2：ClientHello（随机数+套件）-> ServerHello + 证书链 -> 验证证书（CA 链、域名、有效期、吊销）-> 密钥交换（RSA 或 ECDHE）-> 双方算出会话密钥 -> 对称通信；
		非对称加密慢，只用"安全地协商出对称密钥"，海量数据走对称；
		ECDHE 提供前向保密（私钥泄露也解不开历史流量，RSA 密钥交换做不到）；TLS1.3 砍到 1-RTT，会话恢复 0-RTT；
		延伸点：证书链验证、HSTS、企业内网抓包/中间人的场景。

- 跨域的本质？CORS 的简单请求和预检请求区别？credentials 怎么带？

		同源策略是浏览器自己的约束（服务端之间没这事）；
		简单请求（GET/HEAD/POST + 头在白名单 + content-type 限三种）直接发，响应头没Allow-Origin 浏览器拦截；
		非简单（PUT/DELETE、自定义头、application/json）先发 OPTIONS 预检（Max-Age 可缓存预检结果）；
		带 cookie：请求侧 withCredentials / credentials:'include'，响应侧 Allow-Credentials: true 且 Allow-Origin 不能是 *；SameSite=None 必须 Secure，否则第三方上下文 cookie 根本不发；
		开发环境用 Vite proxy（本质反向代理，不存在跨域），生产才谈 CORS。

- CSP（内容安全策略）了解吗？现在防 XSS 的主流手段有哪些？

		CSP 用响应头限定资源来源：script-src/style-src/default-src 'self'；unsafe-inline 基本等于没开，内联脚本走 nonce/hash，report-to 收集违规上报；
		防 XSS 的主流还是：输出侧转义（框架默认转义，dangerouslySetInnerHTML / v-html 是口子）、富文本白名单净化（DOMPurify）、cookie HttpOnly、CSP 兜底；
		新增灾区是 Markdown 渲染和 AI 输出渲染，下面有专题。

- 大模型产品的前端形态做过吗？流式输出（SSE / fetch ReadableStream）、打字机效果、Markdown 增量渲染怎么处理？（字节/阿里 AI 方向）

		流式通道：SSE（text/event-stream 按 data: 分包，注意 [DONE] 哨兵和错误也要走事件）或 fetch + ReadableStream 手动 TextDecoder 解码分块；断线重连配 last-event-id，心跳防代理掐连接；
		打字机：拿到 chunk 别直接逐 token 上屏，攒队列 + rAF 匀速吐，不然长回复抖、重排严重；
		增量 Markdown：代码块/表格没闭合时要容错渲染（补虚拟闭合再截断渲染），全量重解析配合分段 memo，否则每个 token 重渲整棵 DOM 卡死；
		滚动：用户上滑看历史时不强制贴底（stick-to-bottom 状态机）、停止生成（AbortController）、失败重试、会话分页向上加载的滚动锚定（overflow-anchor / 手动补偿 scrollTop）；
		这套已经快成为 2026 年前端面试的"新系统设计题"了。

- LLM 输出的 Markdown 渲染有什么 XSS 风险？怎么防？

		模型可能被 prompt 注入产出 <img onerror>、javascript: 链接、恶意 HTML/SVG 直通；
		姿势：渲染后的 HTML 过 DOMPurify（白名单）、链接协议校验、代码块高亮不要用 innerHTML 直拼、再配 CSP 兜底；
		一句话原则：把模型输出当"用户输入"对待，它真可能是攻击者控制的。

- 你平时用 AI 编程工具吗（Copilot / Cursor / Claude 类）？它改变了你的工作方式吗？

		这题现在必问，面试官在等的是"你自己的方法论"：哪些活交给 AI（样板代码、测试用例、一次性脚本、陌生库探路），哪些必须人脑（架构取舍、性能边界、复杂状态设计、安全判断）；
		加分项：讲得清上下文管理（规则文件、喂哪些文档和示例）、任务拆解粒度、验证习惯（跑测试/对比产物再采信）；
		减分回答："用得挺多的，很方便"。

- 怎么保证 AI 生成代码的质量？Code Review 流程有什么变化？

		防线前移：类型和 lint 门禁本来就越严的仓库，AI 产物质量越高；测试先行或同步生成；
		Review 变化：PR 拆小、除了 diff 还要重点看"为什么这么写"（要求作者对每段负责）、警惕"看起来对"的代码——幻觉 API、竞态、安全模式（拼 SQL、硬编码密钥）；
		底线原则：谁合入谁负责，"AI 写的"不是理由。

- 你觉得 AI 时代前端会被替代吗？你的护城河是什么？（几乎必问的开放题）

		别答"不会"也别答"会"，讲分层：模板页和切图还原这类确定性工作确实被吃掉了；价值上移到：需求拆解与取舍（知道"该做什么"）、复杂交互与性能（AI 目前写不出稳定 60fps 的东西）、系统设计（状态/数据/边界）、跨端与 AI 工程化（Agent、评测、上下文体系）；
		最后落到"我用 AI 的效率本身就是我产出的一部分"——这题考的是认知成熟度，不是立场。

- BFF / Serverless / Edge Runtime 在前端场景里你用过吗？

		BFF：为视图聚合裁剪（首屏 15 次串行变 1 次）、协议转换（下游 gRPC/Thrift），Node 是主力；注意别把业务规则漏进 BFF（职责边界的追问）；
		Serverless/Edge：函数级要注意冷启动和超时；适合渲染聚合、鉴权重定向、A/B 分桶、i18n 路由（Cloudflare/Vercel Edge）；和 RSC/流式渲染结合是现在的趋势（边缘就近取数 + 渲染）；
		追问就是取舍：边缘缓存一致性、日志调试成本、厂商锁定。

- 前端低代码/可视化搭建了解吗？Schema、物料、渲染引擎怎么设计？

		核心三件套：Schema（协议：组件树 + 属性 + 变量/表达式 + 事件）、物料（组件 + 可配置描述，设计器面板读它渲染配置项）、渲染引擎（运行时按 Schema 渲染，同一份 Schema 可以出多端）；
		分层：页面搭建（中后台表单/表格 ROI 最高）、流程编排（审批流/Agent workflow 也算）、生成式（AI 直出页面——和搭建互补，schema 给 AI 当约束和校验）；
		难点在扩展性（物料沙箱、生命周期钩子）和版本/发布/回滚体系。

- Node.js 现在还有什么存在感？说说你的看法。（BFF、CLI、AI 应用层）

		"Node 已死"喊了几年，岗位反而在往全栈回流：BFF/SSR 需求稳定；构建工具链虽然核心在转 Rust（Vite/Rspack/Oxc），但 Node 仍是宿主和生态入口；
		新的增长点是 AI 应用层——Vercel AI SDK、LangChain.js、MCP 服务器基本都是 Node/TS 生态先动；
		Bun 在运行时层搅局（装包/打包/测试一体化、启动快），但主战场还是工程化和 AI 应用层。
		答"前端工程师的 Node 使用面"比答"要不要学 Node"实际得多。


- 讲一个你主导的项目，遇到的最难的技术问题是什么，你怎么解决的？

		这题淘汰的是"背答案的人"——没真做过的人讲不出约束和取舍。用 STAR 讲，但重心放在 T（任务的技术难点）和 A（你的分析路径），别停在 R（结果吹牛）；		难点要选"有决策含量"的：不是"我熬三个通宵写完了"，而是"这里有 A/B 两条路，我基于 X 约束选了 A，代价是 Y，我做了 Z 来兜底"——面试官要听的是判断力和权衡，不是体力；		准备时挑一个能层层下钻的：从业务背景 -> 技术选型 -> 卡点 -> 排查过程 -> 最终方案和遗留风险，每一层都能接住追问，这才是真做过。老题里"技术难点"我保留，但答案要按这个结构重新组织。

- 需求频繁变更 / 产品经理朝令夕改，你怎么应对？

		先分类再应对，不一味抱怨也不无脑接：合理的探索性变更（业务在试错）用架构弹性去接（配置化、可扩展的数据结构、把易变规则外置），把变更成本做低它就不伤你；不合理的反复（同一个点来回改）是上游没想清楚，要用数据和边界把它顶回去；		机制上：变更走影响评估（这个改动影响哪些模块、要多久、挤掉什么），让"改需求"有可见成本而不是动动嘴；小步交付 + 频繁对齐，比攒大招到最后被推翻强——敏捷的价值就在这；		态度：产品经理对结果负责、你对实现负责，目标一致。我能接受为把产品做对而改，不接受的是没评估的拍脑袋——这话当面也会这么说。资深的人答这题透出的是"我能管理需求，不是被动接需求"。

- 你怎么做技术方案评审 / 怎么写一份让别人服气的方案？

		方案不是罗列"我要用什么"，是讲清"为什么这么选"：先摆问题和约束（现状、目标、非目标、硬限制），再给选项（至少 2-3 个可行方案 + 各自的收益/成本/风险），最后给结论和推荐理由——决策过程透明，别人才挑得出毛病也才服；		重点写风险和回滚：什么情况下方案会失效、失效了怎么退、灰度策略、监控点在哪——只写"怎么做不写"会怎样"的方案是不成熟的；用数据和场景佐证，不靠"我觉得业界都用这个"；		评审时：先讲背景和结论对齐目标，再展开，把争议点单列；对不同意见——能被论据说服就改、不能就说清理由，评审的目的是把方案打磨对，不是赢得辩论。这题答得好直接体现架构能力和影响力。

- 上线出了事故，你的处理流程是怎样的？

		顺序是止血优先于追责：先恢复（回滚开关、降级、切流量——呼应前面 CD 的多版本秒回滚），别让故障扩大，第一时间同步相关方（别自己闷头查）；		再定位：靠监控和日志还原现场（错误上报、trace id、变更时间点对齐——多数事故和某次发布相关），找到根因而非症状；		最后复盘（blameless）：不只修这个 bug，要问"为什么会被允许发生"——是不是缺测试、缺灰度、缺监控告警、流程有洞，把改进落到机制上（补个门禁、加个告警）而不是记在某人头上。能主动讲"我在事后加了什么让它不再发生"的人，比只说"我修好了"的人高一档。

- 你怎么衡量前端团队 / 自己这一年的价值？只会写页面怎么体现？

		拒绝"我做了 N 个需求"的产出堆砌，那只是工作量不是价值。分三层讲：业务结果（我做的东西让关键指标动了没有——转化率、性能 CWV、稳定性事故率、开发效率提升）；技术资产（沉淀了什么可复用的东西——组件库、脚手架、规范、把某类活从 3 天降到 3 小时）；影响力（带人、跨团队推动、把踩过的坑变成团队规则）；		关键是建立"前后对比"的可信度量：性能优化就贴优化前后的 Lighthouse/RUM 数据，效率提升就给同类需求交付周期对比，别空口；把技术价值翻译成业务语言（老板不关心你用了什么框架，关心少花多少钱、快多少、稳不稳）——这也是我转产品/方案后最大的体会；		警惕自嗨指标：AI 生成代码占比、组件数量这种容易造假的，要用质量信号（缺陷逃逸率）去平衡。

- 你对未来三年的技术趋势怎么看？（考技术视野）

		这题没有标准答案，考的是你是不是只埋头干活、有没有抬头看。我的判断按确定性排序：AI 深度融入研发是确定的，前端角色从"手写实现"往"定义意图 + 审核约束 + 设计人机协作"迁移，会用 AI 放大产出的人会拉开差距；		技术栈上 Rust 化的工具链（Vite/Rolldown/Turbopack 这条线）还在推进、CSS 原生能力持续吃掉预处理器和 JS 的活（嵌套/容器查询已落地，未来更多）、Web 标准和 AI 边界还在博弈（浏览器本地推理、WebGPU）；不确定性也要诚实：哪些是泡沫、哪些沉淀为标配，现在没人敢说死；		最高分的答法不是预测准，而是展示"我有一套判断框架"（区分营销和本质、看采用曲线、看谁在投入），并说清"无论哪个成，我准备的底层能力是什么"。

- HTTP/2 的头部压缩 HPACK 是什么？为什么 HTTP/2 仍然存在队头阻塞？（米哈游面经）

		HPACK = 静态字典（61 个常用头名值对）+ 动态字典（连接存续期内增量学习）+ Huffman 编码，重复的头只传一个索引，解决的是 HTTP/1 头明文冗余和体积问题；它依赖两端同步的表状态，所以中间代理不能随意改写头；
		队头阻塞的根源换了层：HTTP/2 多路复用建立在单一 TCP 连接上，一个包丢失触发 TCP 重传，所有流都得等它——RST_STREAM 是应用层的，管不了传输层的按序交付；这正是 HTTP/3 把丢包恢复和拥塞控制搬进 QUIC、让每条流独立重传的动机；
		追问常落在 keep-alive：HTTP/1 的长复用的是"连接"不是"并行"，同一连接上请求依旧串行排队，浏览器靠每域名 6 条并发连接硬扛——应用层队头阻塞是 HTTP/2 解决的，传输层的是 HTTP/3 解决的，两件事别混；

- WebSocket 和 HTTP/2 的服务端推送有什么区别？现在 Server Push 还算可用方案吗？（米哈游面经）

		定位完全不同：WebSocket 是应用层全双工通道，双方随时互发消息，适合协同、行情、聊天这类"双向有状态"场景；Server Push 只是服务器单方面提前塞资源进浏览器缓存，服务器对客户端的真实需求一无所知；
		现在的地位要讲实话：Chrome 从 106 移除了 HTTP/2/3 的 Server Push（命中率低、白占带宽），更早停用了 103 Early Hints 的旧形态；替代方案是 1xx Early Hints（握手前先回头省 RTT）、preconnect / preload 声明式预取、以及把推送决策交给缓存友好的静态资源策略；
		选型一句话收束：需要"推给用户的状态客户端会回应"走 WebSocket 或 WebTransport；单向的资源提前到位靠声明式预加载；答得出"Server Push 已死"这个现状判断，说明网络知识没停在背书上；

- TCP 的拥塞控制是怎么做的？UDP 凭什么快，哪些场景应该选 UDP？（米哈游面经）

		TCP 四段式：慢启动（指数涨窗）→ 到阈值转拥塞避免（线性加一）→ 丢包后走快重传快恢复（窗口乘性减，不回起点）→ 超时则退回慢启动起点；再叠上流量控制（接收方窗口 rwnd）和 Nagle / delayed-ACK 这些小动作，拥塞控制管网络容量，流量控制管对端消化能力；
		UDP 快的资本是免掉一切：三次握手、重传、拥塞控制、按序交付都不要，报文各自独立所以没有队头阻塞；代价是"裸奔"，要可靠性就在应用层自建——QUIC 就是这个路线（UDP 上做加密、流、重传、拥塞控制），音视频和游戏则直接容忍丢包换实时性；
		Web 侧的映射表要能报出来：DNS 走 UDP、QUIC/HTTP3 走 UDP、WebRTC 媒体通道走 SRTP/UDP、WebTransport 基于 HTTP/3；最后落到判断：宁可略糊也不能卡的实时场景（推流、远控、协同光标）选 UDP 栈，一字节都不能错的场景老老实实用 TCP；

- 大文件上传怎么实现：分片、秒传、断点续传？（字节面经经典题）

		分片：File.slice 按块切（1-10MB 经验值，结合并发数和网络状况动态调），每片带 文件hash + partIndex + 总数 上传，服务端按片暂存、齐了合并；并发要配调度器（Promise 并发上限控制，这题经常和手写并发控制器连着考）；
		秒传 = 内容寻址：上传前先算整文件 hash（大文件用 spark-md5 分块增量计算，放 Worker 里算别卡主线程）问服务端"有没有"，有就直接返回命中；本质上秒传是去重存储的副产物；
		断点续传 = 状态可查询：服务端记录已收分片列表，恢复时先拉差集只补传缺失片；追问三连提前备好——分片大小怎么定（吞吐与失败重传代价的平衡）、失败怎么重试（指数退避 + 分片级幂等 ID）、怎么防错序和串块（每片独立 hash、服务端校验后再合并）；

- 热门充电站同一时段出现大量预约请求，如何防止资源超卖？（阿里云面经）

		超卖的根因是"查-判-写"三步不原子，解法从下往上三层：DB 层用条件更新（UPDATE ... SET stock = stock - 1 WHERE id = ? AND stock > 0），看影响行数，简单可靠但热点行锁扛不了大流量；
		Redis 层做前置漏斗：DECR 或 Lua 脚本原子扣减（内存操作，天然串行化），挡掉绝大多数无效请求，扣成功再投递 MQ 异步落库创建订单；注意超卖防住了还要防少卖——异步落库失败要回补库存、占位不支付要超时释放；
		前端侧的半场也要说：提交即置灰加防重、进页面领幂等 token 提交时携带（防抖防重放不防并发，别把它当超卖方案讲）、下单排队时轮询把状态收敛；完整答案是一条漏斗：前端拦截 → Redis 原子判定 → MQ 削峰 → DB 兜底；

- B 端和 C 端项目在技术关注点上有什么区别？（阿里面经）

		约束不同决定了技术栈不同：B 端用户固定（企业/内部）、场景复杂、功能密度高，重心在权限体系（菜单-按钮-数据三级）、复杂表单表格的工程化、可配置化和存量系统集成；性能标准是"可用即可"，可维护性标准反而拉满；
		C 端面对的是公网随机用户，路径短、流失快、有竞对，重心在性能与体验指标（LCP / INP 直接挂转化率）、SEO 与分享链路、灰度发布和防刷安全、设备与网络的碎片化兼容；一个按钮慢 200ms 丢的是大盘转化，一个权限配错炸的是内部生产事故，风险模型完全不同；
		面试官问这题其实是在验"你那一半之外的理解"：B 端出身要讲得出 C 端的指标压力，C 端出身要讲得出 B 端的建模复杂度；两边都做过，就把"同一套设计体系和工程基建怎么支撑两端分化"讲出来，这是能带团队的视角；

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

	11.mozilla：     https://developer.mozilla.org/zh-CN/docs/Web/JavaScript

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

	爱机车、爱骑行、爱旅行、爱摄影、爱阅读的前端开发攻城师。

	我的微博：http://weibo.com/920802999
