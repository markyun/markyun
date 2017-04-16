
## 前端自动化构建环境的搭建


为了UED前端团队更好的协作开发同时提高项目编码质量，我们需要将Web前端使用工程化方式构建；

 目前需要一些简单的功能：

		1. 版本控制
		6. 编译SASS
		2. 检查JS
		3. 图片合并
		4. 压缩CSS
		5. 压缩JS


这些都是每个Web项目在构建、开发阶段需要做的事情。前端自动化构建环境可以把这些重复工作一次配置，多次重复执行，极大的提高开发效率。

目前最知名的构建工具： Gulp、Grunt、NPM + Webpack；


		grunt是前端工程化的先驱

		gulp更自然基于流的方式连接任务

		Webpack最年轻，擅长用于依赖管理，配置稍较复杂

		推荐使用Gulp，Gulp基于nodejs中stream，效率更好语法更自然,不需要编写复杂的配置文件



### Use Gulp to automate front-end build tasks


Gulp是基于 Node.js的，需要要安装 Node.js


1、为了确保依赖环境正确，我们先执行几个简单的命令检查。

		node -v
		Node是一个基于Chrome JavaScript V8引擎建立的一个解释器
		检测Node是否已经安装，如果正确安装的话你会看到所安装的Node的版本号

2、接下来看看npm，它是 node 的包管理工具，可以利用它安装 gulp 所需的包

		npm -v
		这同样能得到npm的版本号，装 Node 时已经自动安装了npm


3、开始安装Gulp

		npm install -g gulp
		全局安装 gulp

		gulp -v
		得到gulp的版本号，确认安装成功


基础安装结束
-

4、切换到你的在项目根文件夹下，运行

		npm install gulp --save-dev //将具体的gulp功能插件局部安装项目下


5、安装gulp功能插件依赖包

		npm install gulp-jshint gulp-sass gulp-concat gulp-uglify gulp-rename--save-dev



> gulp功能模块的文件会放在项目所在的目录的./node_modules 下



6、我们目前先使用一些简单的功能：

	    - 检查Javascript
	    - 编译Sass文件
	    - 合并Javascript
	    - 压缩合并并重命名Javascript




> 新建gulpfile.js 配置文件放在项目根目录下

	 演示项目目录结构
		testProject		(项目名称)
		|–.git 			通过git进行版本控制,项目自动生成这个文件
		|–node_modules 	组件包目录
		|–dist 			**发布环境**（编译自动生成的）
		    |–css 		样式文件(style.css style.min.css)
		    |–images 	图片文件(压缩图片\合并后的图片)
		    |–js 		js文件(main.js main.min.js)
		    |–index.html  静态页面文件(压缩html)
		|–src 			**开发环境**
		    |–sass            	sass文件
		    |–images       		图片文件
		    |–js              	js文件
		    |–index.html 		静态文件
		|–gulpfile.js  			gulp配置文件
		|–package.json 			依赖模块json文件,在项目目录下npm install会安装项目所有的依赖模块，简化项目的安装程序




> 现在，项目文件夹都建好，组件也安装完毕了，我们需要编写gulpfile.js文件以指定gulp需要为我们完成什么任务。

		gulpfile.js内容如下：

		// 引入gulp
		var gulp = require('gulp');

		// 引入组件
		var jshint = require('gulp-jshint');//检查js
		var sass   = require('gulp-sass');	//编译Sass
		var concat = require('gulp-concat');//合并
		var uglify = require('gulp-uglify');//uglify 组件（用于压缩 JS）
		var rename = require('gulp-rename');//重命名

		// 检查js脚本的任务
		gulp.task('lint', function() {
		    gulp.src('./js/*.js') //可配置你需要检查脚本的具体名字。
		        .pipe(jshint())
		        .pipe(jshint.reporter('default'));
		});

		// 编译Sass
		gulp.task('sass', function() {
		    gulp.src('./scss/*.scss')
		        .pipe(sass())
		        .pipe(gulp.dest('./css'));//dest()写入文件
		});

		// 合并，压缩js文件
		// 找到 js/ 目录下的所有 js 文件，压缩，重命名，最后将处理完成的js存放在 dist/js/ 目录下
		gulp.task('scripts', function() {
		    gulp.src('./js/*.js')
		        .pipe(concat('all.js'))
		        .pipe(gulp.dest('./dist'))
		        .pipe(rename('all.min.js'))
		        .pipe(uglify())
		        .pipe(gulp.dest('./dist'));

		        console.log('gulp task is done');//自定义提醒信息
		});

		.... // 其他任务类似

		// 定义默认任务,执行gulp会自动执行的任务
		gulp.task('default', function(){
		    gulp.run('lint', 'sass', 'scripts');

		    // 监听js文件变化，当文件发生变化后会自动执行任务
		    gulp.watch('./js/*.js', function(){
		        gulp.run('lint','scripts');
		    });
		});

7、现在，回到命令行窗口，可以直接运行gulp任务了。

		gulp

		这将执行定义的default任务，就和以下的命令式同一个意思

		gulp default

		当然，我们可以运行在gulpfile.js中定义的任意任务，比如，现在单独运行sass任务：

		gulp sass

8、编译会显示Finished,如果你的JS有什么不好的地方它会提醒，避免一些不必要的错误，十分贴心

		常见提醒：
		1.禁止在同一行声明多个变量。
		2.请使用 ===/!==来比较true/false或者数值
		3.使用对象字面量替代new Array这种形式
		4.不要使用全局函数。
		5.Switch语句必须带有default分支
		6.函数不应该有时候有返回值，有时候没有返回值。
		7.For循环必须使用大括号
		8.If语句必须使用大括号
		9.for-in循环中的变量 应该使用var关键字明确限定作用域，从而避免作用域污染。

9、gulp的插件数量很多，后面还可以根据自己的需要进行添加任务


		常用的gulp插件参考
		gulp-imagemin: 		压缩图片
		gulp-ruby-sass: 	支持sass，安装此版本需要安装ruby
		gulp-minify-css: 	压缩css
		gulp-jshint:      	检查js
		gulp-uglify:      	压缩js
		gulp-concat:    	合并文件
		gulp-rename:  		重命名文件
		gulp-htmlmin: 		压缩html
		gulp-clean:      	清空文件夹
		gulp-livereload: 	服务器控制客户端同步刷新（需配合chrome插件LiveReload及tiny-lr）



### Use Git as a project management tool


	安装git， 下载安装包会安装好 Git Shell 和可视化环境

    	http://git-scm.com/download/win

    配置用户名：

		git config --global user.name "Your Name"
		git config --global user.email "email@example.com"

	关联一个到团队的库

		git remote add origin git@github.com:markyun/My-blog.git

	添加文件到仓库，添加全部文件用 . 表示

		git add .

	把文件提交到仓库

		git commit -m " first add project file"

	提交文件到团队仓库

		git push -u origin master //将本地的项目提交到远程仓库中。



以上就完成了前端团队最基本的开发环境搭建和代码提交工作流程。



补充：ZSmart UED Team 的前端开发软件环境 (Windows, Linux, Mac OS X)


	    安装Node.Js、NPM、Ruby、Java 基础环境
		Sublime Text3 + 插件 		  用于编写前端代码
		Google chrome 、Mozilla Firefox + Firebug
		Internet Explorer 			进行兼容测试和预览页面UI、动画效果和交互功能
		Node.js+Gulp 				进行前端自动化构建、JS语法验证、CSS压缩，图片压缩等；
		Koala 						实时编译Less、Sass、Compass、CoffeeScript;
		Github 						存储自己的代码库 、git或SVN用于版本控制和团队Code Review
		Tomcat、DedeAMPZ、MAMP	  进行简单运行环境演示
		Photoshop CC 切图 + Sprites 合并小图标
		XMind 						画出清晰的工作或业务逻辑思维图

（待补充...）