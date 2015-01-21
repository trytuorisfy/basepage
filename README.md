# 基础页面
基础页面放一起了，用的话就直接拖吧 哈哈哈！

master为简单版 就是fis+jquery/zepto

arttpl分支为fis + artTemplate + jquery/zepto（已经包含ajax）


tips:切换分支

    git chekcout 分支名称

简介如下：
都用了[fis](http://fis.baidu.com/)，就是基础版的。按照它的[快速入门](http://fis.baidu.com/docs/beginning/getting-started.html#)就可以了


##master
* fis + jquery/zepto

* tpl文件夹里放的是共用部分，以下代码是执行打包，指定域名，输出到指定路径，到时tml文件夹里的内容是不需要的

      fis release -pDo -d ./output
	
* 不要的js不要放在js文件夹里，默认里面所有的js都会被打包！！

##arttpl分支
* fis + [ArtTemplate](https://github.com/aui/artTemplate) + jquery/zepto(已包含ajax)


###注意事项：
* 把需要的合并的css，js放在正文的html中，比如index.html，而不要放在会插入其中的html中，比如header.html，否则会无法合并。
* 如果合并后发现还多css，那是因为开启了less插件，把less插件关掉，css直接用[koala](http://koala-app.com/index-zh.html)生成就好了。不会用的看我的简易教程[看这里！](http://trytuorisfy.github.io/freezy/koala_course.html)

###代码运行简介如下：


    fis server start
	fis release -wL
	fis release -opD -d ./output 
    
    //不用了可以将服务器清除和关闭
    fis server clean
    fis server stop

