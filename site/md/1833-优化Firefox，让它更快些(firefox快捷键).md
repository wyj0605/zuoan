# 优化Firefox，让它更快些(firefox快捷键) 

1、开启流水线(pipelining)
一般的浏览器在读取网页时是先发送请求，然后等待服务器反馈。而 pipelining 则在服务器回应前很主动的发送多个请求，这样能大大减少载入时间。
开启方法：在 about:config 页面(新开标签页输入 about:config 回车 )，双击更改 network.http.pipelining 和 network.http.proxy.pipelining 值为 true，更改 network.http.pipelining.maxrequests 值为8
(不过从网站方角度我不希望大家都用这个办法，这是以多消耗服务器资源为前提的- -)
2、快速渲染
Firefox3 刚出来时，我经常为它的间歇性卡死苦恼，就是渲染停顿。现在已经没有这个问题了，如果能更快些自然更好。通常花在页面渲染的时间约 0.12秒，还要更快的话，参照如下方法：
在 about:config 页面，右键，选择新建 &amp;gt; 整数(New &amp;gt; Integer)，输入 content.notify.interval 作为属性名，确定，再输入 500000 确定。然后再右键，新建 &amp;gt; 布尔(New &amp;gt; Boolean)，创建值为 content.notify.ontimer 并设置为 true。
3、更快的载入
默认状态下当你不动鼠标不碰键盘超过0.75秒(内容切换阈值)，Firefox 将切换到低功耗模式，它意味着反应变慢但是载入速度加快；那小改小阈值就能改善性能，只需这么干：
在 about:config 页面，右键，选择新建 &amp;gt; 整数(New &amp;gt; Integer)，输入 content.switch.threshold 确定，然后输入值 250000 (1/4秒)，然后确定。
4、不中断
设置了这个你就可以在当前界面还没有完全载入前返回上一步(默认Firefox不允许这么干，载入中后退键是灰色的)，这个 hack 很疯狂，不过你可以了解怎么实现：
在 about:config 页面，右键，新建 &amp;gt; 布尔(New &amp;gt; Boolean)，创建值为 content.interrupt.parsing 并设置为 false 。
5、屏蔽 Flash 动画
很多垃圾站恨不得把所有图都用动画来显示，一闪一闪亮晶晶…… 看起来恶心还拖慢速度。so，你只要装一个叫 Flashblock 的扩展就可以眼不见为净了。
6、增加缓存
Firefox 是把浏览时读取的图片/脚本等内容缓存到内存中的，这是它快速浏览和占用大量内存的原因。如果你想更快而且RAM够大(2GB以上)，就可以考虑加大缓存：
在 about:config 页面，右键，选择新建 &amp;gt; 整数(New &amp;gt; Integer)，输入 browser.cache.memory.capacity 确定，然后输入值 65536，然后确定。最后你需要重启动一下 Firefox。
更极端的是，有人为了更快让这个浏览器直接在内存中运行 …… – -
7、开启跟踪猴子(TraceMonkey)
TraceMonkey 是 Firefox 加速 JS 的功能，它将慢速 Javascript 转化为高速 x86 代码执行——据说比现有模式快20倍。当前版本没有这个功能，如果你不怕浏览器崩溃的话可以冒险试试：
安装最新的测试版 Firefox ，运行并进入 about:config 页面，在过滤器中输入 JIT ，双击将 javascript.options.jit.chrome 和 javascript.options.jit.content to 属性改为 true，然后你就拥有更快的 Firefox JS 引擎鸟。
8、压缩数据
如果你家网速比较慢，你可能感觉网页永远打不开，但我们还是有办法。安装 toonel.net，然后这个聪明的 Java 小程序会通过服务器转发数据(类似移动版 Opera 那样)，让你在牺牲小细节一些图片质量等但是能大大改善浏览速度，当然，还节省了流量。
9、我还希望 Firefox 在后台打开新标签，而不是立刻跳到新标签（又不是立刻有得看，过去干什么？），想回头还得多动手。所以设置了：browser.tabs.loadDivertedInBackground = true
10. Firefox是一个优秀的工具，提供了使用键盘的强力功能，很多时候不需要鼠标，比如下面，就是我最常用的8个Firefox快捷键，你最常用的firefox快捷键是什么呢？
1. ctrl + shift + t :: 打开最后关闭的tab
2. ctrl + 1 … 9 :: 切换到某个tab
3. ctrl + k :: 进入google搜索输入焦点
4. ctrl + w :: 关闭当前tab
5. ctrl + t :: 打开一个新tab
6. ctrl + l :: 进入地址栏
7. ctrl + tab / ctrl + shift + tab :: 循环进入前/后tab
8. ctrl + f :: 查找
/Link

[阅读 HTML 版本](../post-1833.html)
