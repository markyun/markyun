# 前端开发面试题

## <a name='preface'>前言</a> ##


[只看问题点这里 ](http://markyun.github.io/2015/Front-end-Developer-Questions/ "Questions")

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



**前端开发所需掌握知识点概要：**（按进阶层级组织：高级工程师 → 技术专家 Staff → 首席/架构 Principal）

	高级工程师（面谈主力层级，「知其然还知其所以然」）：
		渲染与语言底座 —— 从输入 URL 到首帧：解析、样式、布局、绘制、合成；事件循环与微/宏任务、Promise/async 演进、Proxy/Reflect、V8 隐藏类与分代 GC；
		现代 CSS/HTML —— 盒模型、BFC、层叠上下文、Flex/Grid、容器查询、:has()、@layer、原生嵌套、语义化与无障碍；
		TypeScript 7（Go 原生编译器）—— 类型擦除、结构化类型、泛型与工具类型，类型只在编译期存在、运行时校验交给 Zod；
		框架原理（React 19.2 / Vue 3.5）—— Fiber 可中断协调、Hooks 闭包陷阱、Server Components 边界、Suspense/水合、Actions(useActionState/useOptimistic)、keep-alive、信号化趋势；
		状态与数据 —— URL 状态 / 服务端状态(TanStack Query) / 客户端状态按域选型，不是「上来就 Redux」；
		工程链 —— Node v22+、pnpm 内容寻址存储与幽灵依赖、Vite 8(Rolldown/Rust 打包)与 Rust 工具链生态、ESLint flat + type-aware、缓存与分包；
		性能与安全 —— Core Web Vitals(LCP/INP/CLS，75 分位字段数据)、关键路径与 INP 三段拆解、XSS/CSRF/CSP/SameSite 防御机制；
		网络 —— HTTP/2 多路复用与 HPACK、HTTP/3 QUIC 与队头阻塞、缓存体系、跨域与 WebSocket/SSE；
		质量 —— 测试金字塔(Vitest/Playwright)、错误监控与 RUM、CI/CD 流水线。

	技术专家 Staff（主导跨团队方案与平台能力）：
		大规模应用架构 —— 设计系统、Monorepo 与多产品复用、微前端与模块联邦的适用边界、遗留系统渐进迁移；
		性能与稳定的体系化 —— 度量基线、劣化门禁、容量与降级预案、可观测闭环，而不是一次性优化；
		协作与契约 —— 前后端契约(OpenAPI/类型共享)、技术规范制定与推广、以 Code Review 和工具链放大团队产能；
		跨端与元框架 —— Next/Nuxt SSR/SSG/ISG 的 TTFB 与 SEO 权衡、桌面(Electron/Tauri)、移动(RN/小程序)交付形态选型。

	首席/架构 Principal（技术战略与组织影响力）：
		方向判断 —— Rust 工具链演进、WebAssembly、边缘计算与 Serverless 的引入时机评估；
		AI 工程范式 —— 辅助编程与代码质量治理、Agent 与 harness(context engineering、hooks、评测)、流式产品协议(SSE/AG-UI)、AI 产品前端架构与 Token 成本；
		技术资产与组织 —— 平台化与开源、技术品牌、人才梯队与标准建设、前端在业务大盘中的价值度量。

	（清单只是入口：每一项都要求能讲出机制与取舍，并给出真实项目中的证据；IE、XHTML、XMLHttpRequest 这类历史内容仅在「技术史」语境保留。）


**备注：**

	根据自己需要选择性阅读，面试题是对理论知识的总结，让自己学会应该如何表达。

	资料答案不够正确和全面，欢迎欢迎Star和提交issues。

	格式不断修改更新中。

	在 github 项目的右上角，有三个按钮,分别是 watch、star、fork，新来的同学注意不要用错了，无休止的邮件提醒会给你造成不必要的信息干扰。

	当你选择Watching，表示你以后会关注这个项目的全部动态，以后只要这个项目发生变动，被别人提交了pull request、被发起了issue等情况你都会收到邮件通知。

	star相当于是点赞或收藏，方便以后查找。

	fork表示你想要补充完善这个项目的内容。

	更新记录：
	2026-09-23： 文首「知识点概要」按 高级工程师 → Staff → Principal 三级进阶重构，与题库文件同步；删除 2015 时代「无论工作年头长短」清单（IE 事件模型/XHTML/XMLHttpRequest 等）；
	2026-09-22： 网掘 2025-2026 真实大厂面经（腾讯/字节/拼多多/美团/阿里/米哈游/QQ音乐/Shopee/蔚来）和 AI 编程面经，新增 45 道实战题：hooks/Fiber/setState 批处理/zustand/SSR 水合/Error Boundary、webpack 插件、模块联邦、首屏口径、错误监控上报、埋点、HPACK/拥塞控制/大文件上传/防超卖、B 端 C 端对比、vibe coding（优势五件套/Token 成本/代码泄露/Skills/agent loop/SDD）等，全部配答案；
	2026-09-22： 清理淘汰了一批彻底过时的老题和答案（jQuery/Zepto 源码细节、Backbone/Ember/Meteor、Mustache/Handlebars 模板、requireJS/AMD/CMD、applicationCache 离线储存、改密码黄底之类的 trivia），并去掉重复题目；IE、Weex 按“技术史”保留；
	2026-09-22： 新增《AI 时代的Web工程实践》章节；Agent 与 harness（context engineering、CLAUDE.md、hooks、跨模型）、AI 代码质量与 vibe coding、面向用户的 AI 产品（流式/SSE、AG-UI 事件协议、生成式 UI、断线恢复、TTFT、RAG 前端）等题目和答案，Staff 向深度；同时给 HTML/CSS/JS/TypeScript/框架/工程化/业务各方向各补了一批结合原理和真实场景的进阶题；
        2026-09-22： 荒废多年后的大更新；新增 CSS 新特性（嵌套 / :has() / 容器查询）、TypeScript、Vite 与 Rust 工具链、pnpm、React 18/19、Vue 3、Core Web Vitals、HTTP/3、AI 辅助编程等题目和答案；老答案里过时的部分加了批注；
	2018-01-14： 公司在招聘前端，使用react技术栈；借此机会更新一波前端框架相关的题目；
	2016-10-20： 更新一些已被发现的问题。
	2016-03-25： 新增ECMAScript6 相关问题


### 更新时间:  2026-09-23
		

	爱机车、爱骑行、爱旅行、爱摄影、爱阅读的前端开发攻城师。微博：http://weibo.com/920802999
