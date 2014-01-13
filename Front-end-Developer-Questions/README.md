2014年最新前端开发面试题
======

The last time that refresh: 2014/1/13 12:37:57 
-------

本文主要是由于我最近在找前端开发职位，所以总结了一些常见前端面试（多数来源于网络），希望看的朋友，阅后也要用心钻研其中的原理，重要知识需要系统学习，形成自己的知识链。

###万不可投机取巧。只求当时过关，非长久之计也！


####面试有几点需要注意：（来源 @wintercn）

面试题目会根据你的等级和职位变化，入门级到专家级：范围↑、深度↑、方向↑;
类型： 技术视野、项目细节、理论知识型题，算法题，开放性题，案例题。

进行追问，可以确保问到你开始不懂或者面试官开始不懂为止，这样可以大大延展题目的区分度和深度，知道你的实际能力。因为这种关联知识是长时期的学习，绝对不是临时记得住。

回答问题再棒，面试官（一般是你顶头上司面你），会考虑，我要不要这个人做我的同事？  所以态度很重要。

资深的工程师能把absolute和relative弄混，这样的人不要也罢，因为团队需要的你这个人具有可以依靠的才能（靠谱）。


另外： 

资料刚刚收集，答案有些不够正确和全面，欢迎补充你所知道的答案、技巧、题目；最好是现在网上找不到的。
 

格式不太美观，容我学一下markdown语法再来排版。


 Begin！
 
 
------------------------------------------------------------------
#HTML、CSS部分

        要点：对Web标准的理解、浏览器差异、CSS基本功：布局、盒子模型、选择器优先级及使用、HTML5、CSS3技术等
------------------------------------------------------------------

1. Doctype作用? 严格模式与混杂模式-如何触发这两种模式，区分它们有何意义? 

		（1）、<!DOCTYPE> 声明位于文档中的最前面，处于 <html> 标签之前。告知浏览器的解析器，用什么文档类型 规范来解析这个文档。 

		（2）、严格模式的排版和 JS 运作模式是  以该浏览器支持的最高标准运行。

		（3）、在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止老站点无法工作。

		（4）、DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现。
 


2.行内元素有哪些？块级元素有哪些？ 

		（1） CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，比如div默认display属性值为“block”，成为“块级”元素；span默认display属性值为“inline”，是“行内”元素。 


		（2） 行内元素有：a b span img input select strong（强调的语气）

			  块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p  


3.CSS的盒子模型？


		（1）有两种， IE 盒子模型、标准 W3C 盒子模型；IE 的 content 部分包含了 border 和 pading  （需要加上文档type）;

		（2）盒模型： 内容(content)【宽度和高度】、填充(padding)、边界(margin)、 边框(border).




4.link 和@import 的区别是?


		（1）、link属于XHTML标签，而@import完全是CSS提供的一种方式;

		（2）、页面被加载的时候，link-会同时被加载，而@import引用的CSS会等到页面被加载完再加载;

		（3）、import只有在IE5以上的才能识别，而link是XHTML标签，无兼容问题;

		（4）、link方式的样式的权重 高于@import的权重.




5.CSS 选择符有哪些？哪些属性可以继承？优先级算法如何计算？ em和px有什么关系？


		*   ID 和 Class;
		  
		*   Class 可继承、   font-size font-family color, 列表 UL LI DL DD DT 可继承;

		*   不可继承 ：border padding margin width height ;
		  
		*   优先级就近原则，样式定义最近者为准;

		*   载入样式以最后载入的定位为准;

		   优先级为:
		  
		   !important >  id > class > tag  
		  
		   important 比 内联优先级高
		   
		   
		*   如果父元素定义字体大小12px，子元素定义1em，大小就是12px。
		   



6.如何居中div,如何居中一个浮动元素?


	    *  给div设置一个宽度，然后添加margin:0 auto属性
		
			```css
			div{
				width:200px;
				margin:0 auto;
			 }    
            ```
			 
	    *  设置容器的浮动方式为相对定位
			  确定容器的宽高 宽500 高 300 的层
			  设置层的外边距
			  
			  ```css
			 .Div {
			  Width:500px ; height:300px;
			  Margin: -150px 0 0 -250px;
			  position: absolute;
			  left:50%;
			  top:50%;
			} 
			```

 

7.浏览器的内核分别是什么?经常遇到的浏览器的兼容性有哪些？原因，解决方法是什么，hack 的技巧 ？


		* IE浏览器的内核Trident、 Mozilla的Gecko（跨平台）、google的WebKit、Opera内核Presto（跨平台）；

		* png24为的图片在iE6浏览器上出现背景，解决方案是做成PNG8.

		* 浏览器默认的margin和padding不同。解决方案是加一个全局的*{margin:0;padding:0;}来统一。
		 
		* IE6双边距bug:块属性标签float后，又有横行的margin情况下，在ie6显示margin比设置的大。
	    
	      解决方案是在float的标签样式控制中加入 display:inline;将其转化为行内属性。
		   
		* 浮动ie产生的双倍距离 #box{ float:left; width:10px; margin:0 0 0 100px; 
	    
	     //这种情况之下IE会产生20px的距离，这时需要设置display:inline; //使浮动忽略}
 
		* 渐进识别的方式，从总体中逐渐排除局部。 
      
		* 首先，巧妙的使用“\9”这一标记，将IE游览器从所有情况中分离出来。 接着，再次使用“+”将IE8和IE7、IE6分离开来，这样IE8已经独立识别。
         
         ```css
	          .bb{
	           background-color:#f1ee18;/*所有识别*/
	          .background-color:#00deff\9; /*IE6、7、8识别*/
	          +background-color:#a200ff;/*IE6、7识别*/
	          _background-color:#1e0bd1;/*IE6识别*/
	          
	          }
           ```
  
		*  IE下,可以使用获取常规属性的方法来获取自定义属性,也可以使用getAttribute()获取自定义属性;
          Firefox下,只能使用getAttribute()获取自定义属性.  解决方法:统一通过getAttribute()获取自定义属性.
          
		*  IE下,even对象有x,y属性,但是没有pageX,pageY属性; 
          Firefox下,event对象有pageX,pageY属性,但是没有x,y属性.
		  
		* （条件注释）缺点是在IE浏览器下可能会增加额外的HTTP请求数。

           



8.html5\CSS3有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和 HTML5？



		* HTML5 现在已经不是 SGML 的子集，主要是关于图像，位置，存储，功能的优化和改进。

		* 绘画  canvas 元素
		  
		  用于媒介回放的 video 和 audio 元素
		  
		  本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失；sessionStorage 的数据在浏览器关闭后自动删除
		  
		  语意化更好的内容元素，比如 article、footer、header、nav、section
		  
		  表单控件，calendar、date、time、email、url、search
		  
		  CSS3实现圆角，阴影，对文字加特效，增加了更多的CSS选择器  多背景 rgba
		  
		  新的技术webworker websockt
  
		* 移除的元素
		
		纯表现的元素：basefont，big，center，font, s，strike，tt，u；
		
		对可用性产生负面影响的元素：frame，frameset，noframes；
		
		* 是IE8/IE7/IE6支持通过document.createElement方法产生的标签，可以利用这一特性让这些浏览器支持HTML5新标签，
  
       浏览器支持新标签后，还需要添加标签默认的样式：
	   
		*  当然最好的方式是直接使用成熟的框架、使用最多的是html5shim框架
	 ```css
	   < !--[if lt IE 9]>
	   
	   < script> src="http://html5shim.googlecode.com/svn/trunk/html5.js"</script>
	
	   < ![endif]-->
	   ```



9.你怎么来实现设计图，你认为前端应该如何高质量完成工作? 一个满屏 品 字布局 如何设计?


		* 首先划分成头部、body、脚部；。。。。。 

		* 

	  实现效果图是最基本的工作，精确到2px；
	
	  与设计师，产品经理的沟通和项目的参与
	
	  做好的页面结构，页面重构和用户体验
	
	  处理hack，兼容、写出优美的代码格式
	
	  针对服务器的优化、拥抱 HTML5。
	  
	  
	  

![Stated Clearly Image](http://www.w3school.com.cn/i/html_layout_div.gif)  

  
 


10.常使用的库有哪些？常用的前端开发工具？开发过什么应用或组件？


		* 使用率较高的完备框架有jQuery、YUI、Prototype、Ext.js、Mootools等。尤其是jQuery，超过91%。
 
      轻量级框架有Modernizr、underscore.js、backbone.js、Raphael.js等。（理解这些框架的功能、性能、设计原理）
	  
		* Sublime Text 、Eclipse、Notepad、Firebug、HttpWatch
 
		* 城市选择插件，汽车型号选择插件、幻灯片插件。弹出层。（写过开源程序，加载器，js引擎更好）
 



11.什么是面向对象，有什么特点？


		*  。。。。。
		*  抽象：抽象为了简化问题，简单即美，相信我，人类很笨
		*  继承：为了便于扩展或改写原有的功能   　
	        
	        Object.create()来实际继承,（不会看6） 
	        
	        demo：var Student = Object.create(Person); Person是父类
	
		* 多态：为了便于改写原有的功能
	
		* 封装：组件化，便于理解、替换与复用，因此系统会更加灵活（后文提到封装XXX时，就不具体说这些优点了）
  
		* 数据对象有 属性配置的值。

	　　writable：这个属性的值是否可以改。
	
	　　configurable：这个属性的配置是否可以删除，修改。
	
	　　enumerable：这个属性是否能在for…in循环中遍历出来或在Object.keys中列举出来。
	
	　　value：属性值。

		* 当我们需要一个属性的时，Javascript引擎会先看当前对象中是否有这个属性，如果没有的话，就会查找他的Prototype对象是否有这个属性
    
        ```javascript
	     function clone(proto) {
	
		　　function Dummy() { }
	
		　　Dummy.prototype = proto;
	
		　　Dummy.prototype.constructor = Dummy;
	
		　　return new Dummy(); //等价于Object.create(Person);
	
		 } 
					
	     				function object(old) {
						   function F() {};
						   F.prototype = old;
						   return new F();
						}
						var newObj = object(oldObject);
					
           ```



12.列出display的值 和position的值  相对谁进行定位？


		*可用值的说明
	  block 象块类型元素一样显示。
	  none 缺省值。向行内元素类型一样显示。
	  inline-block 象行内元素一样显示，但其内容象块类型元素一样显示。
	  list-item 象块类型元素一样显示，并添加样式列表标记。
  
		* absolute	
			生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。 
		*fixed	
			生成绝对定位的元素，相对于浏览器窗口进行定位。 
		*relative	
			生成相对定位的元素，相对于其正常位置进行定位。 
		* static	默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right 或者 z-index 声明）。
			inherit	规定应该从父元素继承 position 属性的值。
  



13.页面重构怎么操作？



14.语义化的理解？ W3C标准的理解？ 弹性布局和响应式的理解？



15.HTML5的离线储存？



16.为什么要初始化CSS样式。

		*考虑到浏览器的兼容问题，其实不同浏览器对有些标签的默认值是不同的，如果没对CSS初始化往往会出现浏览器之间的页面差异。
	当然，初始化样式会对SEO有一定的影响，但鱼和熊掌不可兼得，但力求影响最小的情况下初始化。

		*最简单的初始化方法就是： * {padding: 0; margin: 0;} 
	
		*淘宝的样式初始化：
	  ```css
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
	```
	
17.(写)描述一段语义的html代码吧。

		*（HTML5中新增加的很多标签（如：<article>、<nav>、<header>和<footer>等）就是基于这样的设计原则）


		* 语义 HTML 是一种使用正确的元素或标记制作的HTML

			< div id="header">

			< h1>标题< /h1>

			< h2>专注Web前端技术< /h2>

			< /div>


		*语义 HTML 具有以下特性：

		文字包裹在元素中，用以反映内容。例如：
		段落包含在 <p> 元素中。
		顺序表包含在<ol>元素中。
		从其他来源引用的大型文字块包含在<blockquote>元素中。
		HTML 元素不能用作语义用途以外的其他目的。例如：
		<h1>包含标题，但并非用于放大文本。
		<blockquote>包含大段引述，但并非用于文本缩进。
		空白段落元素 ( <p></p> ) 并非用于跳行。
		文本并不直接包含任何样式信息。例如：
		不使用 <font> 或 <center> 等格式标记。
		类或 ID 中不引用颜色或位置。


	
	
#深入题了，一般都不知道：

18.absolute的containing block计算方式跟正常流有什么不同？


	

19.position跟display、margin collapse、overflow、float这些特性相互叠加后会怎么样？




20.对BFC规范的理解？（W3C CSS 2.1 规范中的一个概念,它决定了元素如何对其内容进行定位,以及与其他元素的关 系和相互作用。）





21.iframe有那些缺点？


		*iframe会阻塞主页面的Onload事件；

		*iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。使用iframe之前需要考虑这两个缺点。如果需要使用iframe，最好是通过javascript动态给iframe添加src属性值，这样可以可以绕开以上两个问题。


22.css定义的权重


以下是权重的规则：标签的权重为1，class的权重为10，id的权重为100，以下例子是演示各种定义的权重值：
	 ``` 
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
	```
	
	如果权重相同，则最后定义的样式会起作用，但是应该避免这种情况出现


23.eval是做什么的？有什么理解？


		*避免使用eval，eval非常耗性能。



23.写一个通用的事件侦听器函数




24.99%的网站都需要被重构是那本书上写的？


		*网站重构：应用web标准进行设计（第2版）



25.什么叫优雅降级和渐进增强？





26.Node.js的适用场景




27.WEB应用从服务器主动推送Data到客户端有那些方式？


		html5 websoket
		WebSocket通过Flash
		XHR长时间连接
		XHR Multipart Streaming
		不可见的Iframe
		<script>标签的长时间连接(可跨域)




------------------------------------------------------------------
#JavaScript部分


    要点：  面向对象、继承、闭包、插件、作用域、跨域、原型链、模块化、自定义事件、异步装载回调、模板引擎。新知识：Nodejs等
------------------------------------------------------------------ 
	js的几种数据类型：number,string,boolean,object,undefined
	
	js的常见内置对象类：Date,Array,Math、Number、Boolean、String、Array、RegExp、Function、Object。
	
	js的两个类型判断方法：typeof、instanceof
 
通常可以做一些小练习来判断TA的水平，js 虽然很灵活，但是具体的代码和实现方式能体现出一个人的全局观，随着代码规模的增长，复杂度增加，如何合理划分模块实现功能和接口的能力比较重要。 


1.创建一个对象

```javascript
  function Person(name, age) {
    this.name = name;
    this.age = age;
    this.sing = function() { ... } 
  }
```



2.谈谈This对象的理解。

  




3.事件、IE与火狐的事件机制有什么区别？ （事件冒泡 和事件捕获）如何阻止冒泡？？

  




4.什么是闭包，为什么要用？

		*。。。。。。
   
		*执行闭包后,闭包内部变量会存在,而闭包内部函数的内部变量不会存在.
		```javascript
		  function say667() {
			// Local variable that ends up within closure
			var num = 666;
			var sayAlert = function() { alert(num); }
			num++;
			return sayAlert;
		}
		 
		 var sayAlert = say667();
		 sayAlert()
		 ```
		 执行结果应该弹出的667 
		 
	    Singleton;
		 ```javascript
			 var singleton = function () {
				var privateVariable;
				function privateFunction(x) {
					...privateVariable...
				}
			 
				return {
					firstMethod: function (a, b) {
						...privateVariable...
					},
					secondMethod: function (c) {
						...privateFunction()...
					}
				};
			}();
         ```



5.如何判断一个对象是否属于某个类？


		*使用instanceof、
       if(a instanceof Person){
           alert('yes');
       }



6.new操作符具体干了什么呢?

       ```javascript
		var obj  = {};
		obj.__proto__ = Base.prototype;
		Base.call(obj);	 
		```



7.JSON 的了解




8.js延迟加载的方式有哪些


		*defer和async、动态创建DOM方式（用得最多）、按需异步载入js



	
	
9.ajax 是什么?ajax 的交互模型?同步和异步的区别?如何解决跨域问题?

		*
	  1. 通过异步模式，提升了用户体验
	  
	  2. 优化了浏览器和服务器之间的传输，减少不必要的数据往返，减少了带宽占用
	  
	  3. Ajax引擎在客户端运行，承担了一部分本来由服务器承担的工作，从而减少了大用户量下的服务器负载。
	  
	  2. Ajax的最大的特点是什么。
	  
	  Ajax可以实现动态不刷新（局部刷新）
	  readyState属性   请求的状态 有5个可取值： 0=未初始化 ，1=正在加载 2=以加载，3=交互中，4=完成
  
		*ajax的缺点
  
	  1、ajax不支持浏览器back按钮。
	  
	  2、安全问题 AJAX暴露了与服务器交互的细节。
	  
	  3、对搜索引擎的支持比较弱。
	  
	  4、破坏了程序的异常机制。
	  
	  5、不容易调试。
	
		*跨域： jsonp、 iframe、window.name、HTML5中新引进的window.postMessage、服务器上设置代理页面




10.模块化怎么做？





11.对Node的优点和缺点提出了自己的看法：


		*（优点）因为Node是基于事件驱动和无阻塞的，所以非常适合处理并发请求，因此构建在Node上的代理服务器相比其他技术实现（如Ruby）的服务器表现要好得多。此外，与Node代理服务器交互的客户端代码是由javascript语言编写的，因此客户端和服务器端都用同一种语言编写，这是非常美妙的事情。

		*（缺点）Node是一个相对新的开源项目，所以不太稳定，它总是一直在变，而且缺少足够多的第三方库支持。看起来，就像是Ruby/Rails当年的样子。




12.异步加载的方式
 

  (1) defer，只支持IE
  
  (2) async：
  
  (3) 创建script，插入到DOM中，加载完毕后callBack
  
  documen.write和 innerHTML的区别
  
  document.write只能重绘整个页面
  
  innerHTML可以重绘页面的一部分
  


13.告诉我答案是多少？

	(function(x){
		delete x;
		alert(x);
	})(1+5);
	函数参数无法delete删除，delete只能删除通过for in访问的属性。当然，删除失败也不会报错，所以代码运行会弹出“1”。
	

	
14.JS中的call()和apply()方法的区别？


  例子中用 add 来替换 sub，add.call(sub,3,1) == add(3,1) ，所以运行结果为：alert(4); 

  注意：js 中的函数其实是对象，函数名是对 Function 对象的引用。
```javascript
	function add(a,b)
	{
	    alert(a+b);
	}
	
	function sub(a,b)
	{
	    alert(a-b);
	}
	
	add.call(sub,3,1); 
``` 


15.Jquery与jQuery UI 有啥区别？


		*jQuery是一个js库，主要提供的功能是选择器，属性修改和事件绑定等等。

		*jQuery UI则是在jQuery的基础上，利用jQuery的扩展性，设计的插件。提供了一些常用的界面元素，诸如对话框、拖动行为、改变大小行为等等


16.jquery 中如何将数组转化为json字符串，然后再转化回来？


jQuery中没有提供这个功能，所以你需要先编写两个jQuery的扩展：
```javascript
$.fn.stringifyArray = function(array) {
    return JSON.stringify(array)
}

$.fn.parseArray = function(array) {
    return JSON.parse(array)
}
```
然后调用：
$("").stringifyArray(array)



17.JavaScript中的作用域与变量声明提升？





------------------------------------------------------------------
#其他部分

    （正则、优化、重构、响应式、移动端、团队协作、SEO、UED、职业生涯）
------------------------------------------------------------------

		*基于Class的选择性的性能相对于Id选择器开销很大，因为需遍历所有DOM元素。

		*频繁操作的DOM，先缓存起来再操作。用Jquery的链式调用更好。    比如：var str=$("a").attr("href");

		*前端开发的优化问题（雅虎14条性能优化原则）。

	  （1） 减少http请求次数：CSS Sprites, JS、CSS源码压缩、图片大小控制合适；网页Gzip，CDN托管，data缓存 ，图片服务器。
	
	  （2） 前端模板 JS+数据，减少由于HTML标签导致的带宽浪费，前端用变量保存AJAX请求结果，每次操作本地变量，不用请求，减少请求次数
	
	  （3） 用innerHTML代替DOM操作，减少DOM操作次数，优化javascript性能。
	
	  （4） 当需要设置的样式很多时设置className而不是直接操作style。
	
	  （5） 少用全局变量、缓存DOM节点查找的结果。减少IO读取操作。
	
	  （6） 避免使用CSS Expression（css表达式)又称Dynamic properties(动态属性)。
	
	  （7） 图片预加载，将样式表放在顶部，将脚本放在底部  加上时间戳。
	
	  （8） 避免在页面的主体布局中使用table，table要等其中的内容完全下载之后才会显示出来，显示比div+css布局慢。
	 
	 
 
 4.


11.谈谈你认为怎样做能是项目做的更好？



12.你对前端界面工程师这个职位是怎么样理解的？它的前景会怎么样？



13.加班的看法

    加班就像借钱，原则应当是------救急不救穷
	

	
14.平时如何管理你的项目，如何设计突发大规模并发架构？

  		*
	先期团队必须确定好全局样式（globe.css），编码模式(utf-8) 等

	编写习惯必须一致（例如都是采用继承式的写法，单样式都写成一行）；

	标注样式编写人，各模块都及时标注（标注关键样式调用的地方）；

	页面进行标注（例如 页面 模块 开始和结束）；

	CSS跟HTML 分文件夹并行存放，命名都得统一（例如style.css）

	JS 分文件夹存放 命民以该JS 功能为准英文翻译；

	图片采用整合的 images.png png8 格式文件使用 尽量整合在一起使用方便将来的管理

	 
	 
15.你说你热爱前端，那么应该WEB行业的发展很关注吧？ 说说最近最流行的一些东西吧？

	
16.你有了解我们公司吗？说说你的认识？

   因为我想去阿里，所以我针对阿里的说
	
	：最羡慕就是在双十一购物节，350.19亿元，每分钟支付79万笔。海量数据，居然无一漏单、无一故障。太厉害了。

	
   作为一名前端工程师，无论工作年头长短都应该必须掌握的知识点有：
   
		1、DOM结构 —— 两个节点之间可能存在哪些关系以及如何在节点之间任意移动。
		
		2、DOM操作 ——如何添加、移除、移动、复制、创建和查找节点等。
		
		3、事件 —— 如何使用事件，以及IE和标准DOM事件模型之间存在的差别。
		
		4、XMLHttpRequest —— 这是什么、怎样完整地执行一次GET请求、怎样检测错误。
		
		5、严格模式与混杂模式 —— 如何触发这两种模式，区分它们有何意义。
		
		6、盒模型 —— 外边距、内边距和边框之间的关系，及IE8以下版本的浏览器中的盒模型
		
		7、块级元素与行内元素 —— 怎么用CSS控制它们、以及如何合理的使用它们
		
		8、浮动元素——怎么使用它们、它们有什么问题以及怎么解决这些问题。
		
		9、HTML与XHTML——二者有什么区别，你觉得应该使用哪一个并说出理由。
		
		10、JSON —— 作用、用途、设计结构。
		
		
		他们也许不懂交互设计，但是没人比他们懂交互设计的实现，和每一个细节。
		他们也许不懂视觉设计，但是没人比他们懂视觉设计如何变为现实。
		他们也许不懂后台数据库，但是他们其实才是数据的第一消费者。
		他们也许不是产品经理，但是产品的质量几乎都是由他们来决定。
		
		
		什么都略懂一点生活更美好！
		
		
		不断完善中。
		
		喜欢骑行、旅行、摄影、行为心理学，前端开发攻城师。
		
		联系微博：http://weibo.com/920802999
