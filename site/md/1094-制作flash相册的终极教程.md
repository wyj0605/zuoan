# 制作flash相册的终极教程 

说终极是大话了，因为真正的高手可以用Flash软件直接制作出千变万化的相册。这里讲的是取巧的方法，也就是如果有像我这样菜鸟也想自己拥有一个flash相册，有什么软件可以作到吗？
找到两种方法：
一、是ilank介绍的一个很不错的flash相册展示效果，他提供monoslideshow1.32商业版相册的下载：
使用步骤：
第一步：把monoslideshow文件夹上传到blog目录中(博客安在哪个目录，就上传到哪个目录)
第二步:PJblog（wordpress也适用）日志中的写法（FCKeditor编辑器唯一写法，效果只支持IE，不支持FF,因为编辑器会过滤掉embed,没办法）,代码如下
&amp;lt;object codebase=”http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=7,0,19,0″ height=”360″ width=”480″ classid=”clsid:D27CDB6E-AE6D-11cf-96B8-444553540000″&amp;gt;
&amp;lt;param value=”monoslideshow/monoslideshow.swf” name=”movie” /&amp;gt;&amp;lt;!–flash的路径”–&amp;gt;
&amp;lt;param value=”high” name=”quality” /&amp;gt;
&amp;lt;param value=”monoslideshow/play_img/” name=”base” /&amp;gt; &amp;lt;!–xml路径,默认为”monoslideshow/play_img/”,你也可以写成”monoslideshow/play_img- 2/”–&amp;gt;
&amp;lt;param value=”application/x-shockwave-flash” name=”TYPE” /&amp;gt;
&amp;lt;param value=”#1f1f1f” name=”bgcolor” /&amp;gt;&amp;lt;/object&amp;gt;
★如果是在后台建模块，博客模块代码写法(效果同时支持IE、FF，日志中不能这样写的原因是，编辑器会过滤掉base=”monoslideshow/play_img/”，这样就不能读取xml)
&amp;lt;embed type=”application/x-shockwave-flash” src=”monoslideshow/monoslideshow.swf” id=”SOmonoSlideshow” name=”SOmonoSlideshow” bgcolor=”#1f1f1f” quality=”high” base=”monoslideshow/play_img/” height=”360″ width=”480″&amp;gt;
重要说明：
monoslideshow/play_img/monoslideshow.xml 文件里的图片路径请自行更改测试。
monoslideshow/play_img/images/ 里为展示图片
你可以在monoslideshow放两个、三个或更多的play_img（名字自己随便取）文件夹相册，重要的就只有两个路径，一个flash路径【src=”monoslideshow/monoslideshow.swf”】和xml路径【base=”monoslideshow/play_img/”】
参考网站 http://www.monoslideshow.com 参数超级多，不过设置很简单，你可以前往在线调试参数下载xml。
下载地址：http://ilank.googlecode.com/files/monoslideshow1.32.rar
内有商业版PDF使用说明书，和两个例子，这个相册有N种效果，需要调节xml参数来设置。
二、利用  Flash Slideshow Maker打造炫目FLASH相册
如今在网络上最常见的相册可不是以前那种相册本，而是由相片组成的带有声音和图像的FLASH相册。怎么样通过简单的操作来打造属于自己的FLASH相册呢？这里为大家推荐一款FLASH相册制作软件——Flash Slideshow Maker，它可以让我们通过简单的操作即可为自己打造出绚丽的FLASH相册效果！
教程看这里——打造炫目FLASH相册  Flash Slideshow Maker
华军下载： 点击即可下载
序列号大家就自己找吧！
这是里面的一种效果，这些图片引用自“有意思吧”里的这篇文章——历史这坛8卦的酒，别有一番味道在心头！
作者云：最近有点迷中国的历史，发现历史真是个大宝藏，能发现许多有 意思的事情。忽然冒出一个8卦下历史趣事的想法，用现在的观点去看历史应该是别有一番味道。唐太宗说：以古为鉴，可知兴替。地瓜熊说：以史为酒，轻酌娱人，细品育己。历史的经验告诉我们，真相多在8卦中……

[阅读 HTML 版本](../post-1094.html)
