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