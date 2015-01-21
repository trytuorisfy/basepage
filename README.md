# fis + ArtTemplate +jquery/zepto 基础页面

简直救人于水火arttemplate的教程→[看这里！](http://www.cnblogs.com/Fengger/p/3826241.html)

对了，有个重点就是直接数据取到要的那部分，就直接一个each循环了
类似这种

    {
        "data":{
	        "list":[
	            {
	                "tit":"我是图片一",
	                "url":"http://tuorisfy.qiniudn.com/jianshu/html/images/1.jpg"
	            },
	            {
	                "tit":"我是图片二",
	                "url":"http://tuorisfy.qiniudn.com/jianshu/html/images/2.jpg"
	            },
	            {
	                "tit":"我是图片三",
	                "url":"http://tuorisfy.qiniudn.com/jianshu/html/images/3.jpg"
	            },
	            {
	                "tit":"我是图片四",
	                "url":"http://tuorisfy.qiniudn.com/jianshu/html/images/4.jpg"
	            }
	        ]
	    }
	}

    

    $(function(){
        $.getJSON('datas.json', function(data)
            {
                var html = template('pic-tpl', {
                    error:data.error,
                    list: data.data.list//直接定位到要的那部分！
                });
                $('#pics').html(html);
            }
        );
      });
    
##注意事项
* 由于里面直接引入了json，fis 打包后的页面直接拖入浏览器上没东西，就用firefox看，chrome读不到json。
* 再叨叨一句，不要的js打包的时候不要放到js文件夹里面！