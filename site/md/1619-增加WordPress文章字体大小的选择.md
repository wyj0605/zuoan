# 增加WordPress文章字体大小的选择 

在留言板 中idk 说文章的字体太小，很伤眼睛，我本来想借用插件的方法，找了一下，好像没有专门提供这一功能的插件，就自己写了一小段代码，基本能满足这一功能。
方法很简单：
打开single.php文件，在&amp;lt;?php get_header(); ?&amp;gt;下面插入以下Js代码：
&amp;lt;script type=&quot;text/javascript&quot;&amp;gt;
function SetFont(size){
	document.getElementById(&quot;logPanel&quot;).style.fontSize=size
}
&amp;lt;/script&amp;gt;
在你想提供改变字体大小按钮的地方插入以下代码：
字体大小: &amp;lt;a href=”javascript:SetFont(’12px’)” accesskey=”1″&amp;gt;小&amp;lt;/a&amp;gt; &amp;lt;a href=”javascript:SetFont(’14px’)” accesskey=”2″&amp;gt;中&amp;lt;/a&amp;gt; &amp;lt;a href=”javascript:SetFont(’16px’)” accesskey=”3″&amp;gt;大&amp;lt;/a&amp;gt;
在你显示文章内容部分的&amp;lt;div&amp;gt;&amp;lt;/div&amp;gt;增加一个id=”logPanel”标识，一般是这样写的：&amp;lt;div id=”logPanel” class=”content”&amp;gt; 显示文章内容代码&amp;lt;/div&amp;gt;

[阅读 HTML 版本](../post-1619.html)
