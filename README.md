## 前端相关的工具

1.调试工具 Firebug lite

compatible：IE6+, Firefox, Opera, Safari and Chrome

引用方法：

1).加入标签，在需要的页面单击标签运行。

标签地址：
	
	javascript:(function(F,i,r,e,b,u,g,L,I,T,E){if(F.getElementById(b))return;E=F[i+'NS']&&F.documentElement.namespaceURI;E=E?F[i+'NS'](E,'script'):F[i]('script');E[r]('id',b);E[r]('src',I+g+T);E[r](b,u);(F[e]('head')[0]||F[e]('body')[0]).appendChild(E);E=new%20Image;E[r]('src',I+L);})(document,'createElement','setAttribute','getElementsByTagName','FirebugLite','4','firebug-lite.js','releases/lite/latest/skin/xp/sprite.png','https://getfirebug.com/','#startOpened');

2).在页面头部引入firebug lite的js代码

	<script type="text/javascript" src="https://getfirebug.com/firebug-lite.js"></script>

3).引入下载的本地firebug lite代码

	<script type="text/javascript" src="/local/path/to/firebug-lite.js"></script>