 
##The last time that refresh: 2014-01-07  

本文主要是由于我最近在找前端开发职位，所以总结了一些常见前端面试的基本理论知识和一些经验，希望看的朋友，阅之后也要用心钻研其中的原理，
不可投机取巧，只求面试过关，非长久之计也！

另外： 
欢迎补充你所知道的技巧、题目、答案；最好是现在网上找不到的。
 


------------------------------------------------------------------
#HTML、CSS部分

        要点：对Web标准的理解、浏览器差异、CSS基本功：布局、盒子模型、选择器优先级及使用、HTML5、CSS3技术等
------------------------------------------------------------------

1. Doctype?严格模式不混杂模式-如何触发这两种模式，区分它们有何意义?
【

（1）、<!DOCTYPE> 声明位于文档中的最前面，处于 <html> 标签之前。告知浏览器的解析器，用什么文档类型 规范来解析这个文档。 

（2）、严格模式的排版和 JS 运作模式是  以该浏览器支持的最高标准运行。

（3）、在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止老站点无法工作。

（4）、DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现。
】


2.行内元素有哪些？块级元素有哪些？
【


（1）CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，比如div默认display属性值为“block”，成为“块级”元素；span默认display属性值为“inline”，是“行内”元素。 


（2）行内元素有：a b span I bem img input select strong（强调的语气）

    块级元素有：div ul ol lidl dt dd h1 h2 h3 h4…p
】

3.CSS的盒子模型？
【

（1）有两种， IE 盒子模型、标准 W3C 盒子模型；IE 的 content 部分包含了 border 和 pading  （需要加上文档type）

（2）盒模型： 内容(content)的宽度和高度、填充(padding)、边界(margin)、 边框(border)、
】


4.link 和@import 的区别是?
【

（1）、link属于XHTML标签，而@import完全是CSS提供的一种方式

（2）、页面被加载的时候，link-会同时被加载，而@import引用的CSS会等到页面被加载完再加载。

（3）、import只有在IE5以上的才能识别，而link是XHTML标签，无兼容问题。

（4）、link方式的样式的权重 高于@import的权重
】


5.CSS 选择符有哪些？哪些属性可以继承？优先级算法如何计算？
【

  ID 和 Class
  Class 可继承、   font-size font-family color可以继承  列表 UL LI DL DD DT 可继承

  不可继承 ：border padding margin width height 
  
  优先级就近原则，样式定义最近者为准

  载入样式以最后载入的定位为准

  优先级为
  !important >  id > class > tag  
   important 比 内联优先级高
】


6.如何居中div,如何居中一个浮动元素?
【

 （1） 给div设置一个宽度，然后添加margin:0 auto属性
         如：div{ width:200px; margin:0 auto;}

 （2） 设置容器的浮动方式为相对定位
          确定容器的宽高 宽500 高 300 的层
          设置层的外边距
         .Div {
          Width:500px ; height:300px;
          Margin: -150px 0 0 -250px;
          position: absolute;
          left:50%;
          top:50%;
        }
】
 

7.浏览器的内核分别是什么?经常遇到的浏览器的兼容性有哪些？原因，解决方法是什么，hack 的技巧 ？
【

（1）  IE浏览器的内核Trident、 Mozilla的Gecko（跨平台）、google的WebKit、Opera内核Presto（跨平台）；

（2）   1.png24为的图片在iE6浏览器上出现背景，解决方案是做成PNG8.

	    2.浏览器默认的margin和padding不同。解决方案是加一个全局的*{margin:0;padding:0;}来统一。
		 
	    3.IE6双边距bug:块属性标签float后，又有横行的margin情况下，在ie6显示margin比设置的大。
	      解决方案是在float的标签样式控制中加入 display:inline;将其转化为行内属性。
		   
	    4.浮动ie产生的双倍距离 #box{ float:left; width:10px; margin:0 0 0 100px; 
	     //这种情况之下IE会产生20px的距离，这时需要设置display:inline; //使浮动忽略}
              
 （3）渐进识别的方式，从总体中逐渐排除局部。
      首先，巧妙的使用“\9”这一标记，将IE游览器从所有情况中分离出来。
	   接着，再次使用“+”将IE8和IE7、IE6分离开来，这样IE8已经独立识别。
          demo：
          .bb{
           background-color:#f1ee18;/*所有识别*/
          .background-color:#00deff\9; /*IE6、7、8识别*/
          +background-color:#a200ff;/*IE6、7识别*/
          _background-color:#1e0bd1;/*IE6识别*/
          
          }
          
（4）  IE下,可以使用获取常规属性的方法来获取自定义属性,也可以使用getAttribute()获取自定义属性;
          Firefox下,只能使用getAttribute()获取自定义属性.  解决方法:统一通过getAttribute()获取自定义属性.
          IE下,even对象有x,y属性,但是没有pageX,pageY属性; 
          Firefox下,event对象有pageX,pageY属性,但是没有x,y属性.

           
】


8.html5\CSS3有哪些新特性？
【

（1） HTML5其实就是关于图像，位置，存储，功能，速度的优化和改进。

（2）
  绘画  canvas 元素
  用于媒介回放的 video 和 audio 元素
  本地离线存储
  语意化更好的内容元素，比如 article、footer、header、nav、section
  表单控件，calendar、date、time、email、url、search
  CSS3实现圆角，阴影，对文字加特效，增加了更多的CSS选择器  多背景 rgba
  新的技术webworker websockt
】


9.你怎么来实现设计图，如何高质量完成页面和脚本?
【

（1）首先划分成头部、body、脚部；。。。。。 

（2）

  实现效果图是最基本的工作，精确到2px；

  与设计师，产品经理的沟通和项目的参与

  做好的页面结构，页面重构和用户体验

  处理hack，兼容、写出优美的代码格式

  针对服务器的优化、拥抱 HTML5。
】 


10.常使用的库有哪些？常用的前端开发工具？开发过什么应用或组件？
【

 （1）jquery 、ExtJS、easyui、kissy （淘宝）  
 （2）Sublime Text 、Eclipse、Notepad、Firebug、HttpWatch
 （3）城市选择插件，汽车型号选择插件、幻灯片插件。弹出层。
】


11.什么是面向对象，有什么特点？
【

  （1）一切都是对象。
  （2） 
  抽象：抽象为了简化问题，简单即美，相信我，人类很笨

  继承：为了便于扩展或改写原有的功能   　　Object.create()来实际继承,（不行就看6） demo：var Student = Object.create(Person); Person是父类

  多态：为了便于改写原有的功能

  封装：组件化，便于理解、替换与复用，因此系统会更加灵活（后文提到封装XXX时，就不具体说这些优点了）
  
  （3） 数据对象有 属性配置的值。

　　writable：这个属性的值是否可以改。

　　configurable：这个属性的配置是否可以删除，修改。

　　enumerable：这个属性是否能在for…in循环中遍历出来或在Object.keys中列举出来。

　　value：属性值。

   （4）当我们需要一个属性的时，Javascript引擎会先看当前对象中是否有这个属性，如果没有的话，就会查找他的Prototype对象是否有这个属性
   
   （5）  
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

】


12.列出display的值 和position的值  相对谁定位？
【

 （1）  可用值的说明
  block 象块类型元素一样显示。
  none 缺省值。向行内元素类型一样显示。
  inline-block 象行内元素一样显示，但其内容象块类型元素一样显示。
  list-item 象块类型元素一样显示，并添加样式列表标记。
  
 （2） absolute	
  生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。 
  fixed	
  生成绝对定位的元素，相对于浏览器窗口进行定位。 
  relative	
  生成相对定位的元素，相对于其正常位置进行定位。 
  static	默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right 或者 z-index 声明）。
  inherit	规定应该从父元素继承 position 属性的值。
】


13.页面重构怎么操作？



14.语义化的理解？ W3C 标准的理解？ 



15、HTML5的离线储存？



16、为什么要初始化CSS样式。

	考虑到浏览器的兼容问题，其实不同浏览器对有些标签的默认值是不同的，如果没对CSS初始化往往会出现浏览器之间的页面差异。
	当然，初始化样式会对SEO有一定的影响，但鱼和熊掌不可兼得，但力求影响最小的情况下初始化。

	最简单的初始化方法就是： * {padding: 0; margin: 0;} 
	
	
------------------------------------------------------------------
#JavaScript部分


    要点：  面向对象、继承、闭包、插件、作用域、跨域、原型链、模块化、自定义事件、异步装载回调、模板引擎。新知识：Nodejs等
------------------------------------------------------------------ 
js的几种数据类型：number,string,boolean,object,undefined五种数据类型

js的常见内置对象类：Date,Array,Math、Number、Boolean、String、Array、RegExp、Function、Object。

js的两个类型判断方法：typeof、instanceof
 
通常可以做一些小练习来判断TA的水平，js 虽然很灵活，但是具体的代码和实现方式能体现出一个人的全局观，随着代码规模的增长，复杂度增加，如何合理划分模块实现功能和接口的能力比较重要。 


1.创建一个对象
【

  function Person(name, age) {
    this.name = name;
    this.age = age;
    this.sing = function() { ... } 
  }

】


2.谈谈This对象的理解。
【
  

】


3.事件、IE与火狐的事件机制有什么区别？ （事件冒泡 和事件捕获）如何阻止冒泡？？
【
  

】


4.什么是闭包？
【

  （1）闭包就是在函数执行后，函数的“堆栈”的数据并不释放（在内存中维持一个变量）
  （2）这个函数的局部变量全部集合在闭包内、保护函数内的变量安全
  （3）当在一个函数内定义另外一个函数就会产生闭包
  （4）可以把外层函数理解成一个类，变量理解为静态成员，内部函数是成员方法。 
  （5） 闭包返回的函数内部不能有return.(因为这样就真的结束了)
        执行闭包后,闭包内部变量会存在,而闭包内部函数的内部变量不会存在.
		  function say667() {
			// Local variable that ends up within closure
			var num = 666;
			var sayAlert = function() { alert(num); }
			num++;
			return sayAlert;
		}
		 
		 var sayAlert = say667();
		 sayAlert()
		 执行结果应该弹出的667 
		 
		 Singleton ：
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

】


5.如何判断一个对象是否属于某个类？
【

    使用instanceof、使用constructor
       if(a instanceof Person){
           alert('yes');
       }
】


6.new操作符具体干了什么呢?
【

		var obj  = {};
		obj.__proto__ = Base.prototype;
		Base.call(obj);	 
】


7.JSON 的了解
【

】

8.js延迟加载的方式有哪些
【

defer和async、动态创建DOM方式（用得最多）、按需异步载入js
】

	
	
5.ajax 是什么?ajax 的交互模型?同步和异步的区别?如何解决跨域问题?
【

  1. 通过异步模式，提升了用户体验
  
  2. 优化了浏览器和服务器之间的传输，减少不必要的数据往返，减少了带宽占用
  
  3. Ajax引擎在客户端运行，承担了一部分本来由服务器承担的工作，从而减少了大用户量下的服务器负载。
  
  2. Ajax的最大的特点是什么。
  
  Ajax可以实现动态不刷新（局部刷新）
  readyState属性   请求的状态 有5个可取值： 0=未初始化 ，1=正在加载 2=以加载，3=交互中，4=完成
  
  ajax的缺点
  
  1、ajax不支持浏览器back按钮。
  
  2、安全问题 AJAX暴露了与服务器交互的细节。
  
  3、对搜索引擎的支持比较弱。
  
  4、破坏了程序的异常机制。
  
  5、不容易调试。

 跨域： jsonp、 iframe、window.name、HTML5中新引进的window.postMessage、服务器上设置代理页面

】


6.模块化怎么做？
【

】


7.对Node的优点和缺点提出了自己的看法：
【

（优点）因为Node是基于事件驱动和无阻塞的，所以非常适合处理并发请求，因此构建在Node上的代理服务器相比其他技术实现（如Ruby）的服务器表现要好得多。此外，与Node代理服务器交互的客户端代码是由javascript语言编写的，因此客户端和服务器端都用同一种语言编写，这是非常美妙的事情。

（缺点）Node是一个相对新的开源项目，所以不太稳定，它总是一直在变，而且缺少足够多的第三方库支持。看起来，就像是Ruby/Rails当年的样子。
】


8.异步加载的方式
【 

  (1) defer，只支持IE
  
  (2) async：
  
  (3) 创建script，插入到DOM中，加载完毕后callBack
  
  documen.write和 innerHTML的区别
  
  document.write只能重绘整个页面
  
  innerHTML可以重绘页面的一部分
】



------------------------------------------------------------------
#其他部分

    （正则、优化、重构、响应式、移动端、团队协作、SEO、UED、职业生涯）
------------------------------------------------------------------

1、基于Class的选择性的性能相对于Id选择器开销很大，因为需遍历所有DOM元素。
2、频繁操作的DOM，先缓存起来再操作。用Jquery的链式调用更好。    比如：var str=$("a").attr("href");

3、前端开发的优化问题（雅虎14条性能优化原则）。
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
	

	
14.如何设计突发大规模并发架构？

	 
	 
	
	
	
	
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
待完善、、、、、、、
微博：http://weibo.com/920802999
