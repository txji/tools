## 前端相关的工具

###1.调试工具 Firebug lite

compatible：IE6+, Firefox, Opera, Safari and Chrome

引用方法：

1).加入标签，在需要的页面单击标签运行。

标签地址：
	
	javascript:(function(F,i,r,e,b,u,g,L,I,T,E){if(F.getElementById(b))return;E=F[i+'NS']&&F.documentElement.namespaceURI;E=E?F[i+'NS'](E,'script'):F[i]('script');E[r]('id',b);E[r]('src',I+g+T);E[r](b,u);(F[e]('head')[0]||F[e]('body')[0]).appendChild(E);E=new%20Image;E[r]('src',I+L);})(document,'createElement','setAttribute','getElementsByTagName','FirebugLite','4','firebug-lite.js','releases/lite/latest/skin/xp/sprite.png','https://getfirebug.com/','#startOpened');

2).在页面头部引入firebug lite的js代码

	<script type="text/javascript" src="https://getfirebug.com/firebug-lite.js"></script>

3).引入下载的本地firebug lite代码

	<script type="text/javascript" src="/local/path/to/firebug-lite.js"></script>

###2.截图测量工具 FSCapture

###3.常用标签类工具

* 获取页面中DOM的数量

		javascript:(function(){alert(document.getElementsByTagName('*').length);})();

* 获取页面中IMG的数量

		javascript:(function(){alert(document.getElementsByTagName('img').length);})();

* 查看透明图片时，方便查看白色部分

		javascript:(function(){document.body.style.backgroundColor='#aaa'})();

###4.对比工具 BCompare

###5.截图生成GIF工具 GifCam / LICEcap

###6.Ctrip IMG Zip Tools(imgzip2012-6-4.7z)

###7.获取性能参数

	javascript:(function(){
	    if(!window.performance){
	        alert('您的浏览器暂不支持window.performance,请更换浏览器试试！');
	    }else{
	        var Dns=0,Connect=0,Request=0,Response=0,Blank=0,domContentLoaded=0,Onload=0,Timeline=window.performance.timing;
	        function TimeChange(input){
	            if(typeof(input) != 'number'){return NaN;}
	            if(input < 1000){
	                return input + 'ms';
	            }else{
	                return (input/1000).toFixed(2) + 's';
	            }
	        }
	        Dns=TimeChange(Timeline.domainLookupEnd-Timeline.domainLookupStart);
	        Connect=TimeChange(Timeline.connectEnd-Timeline.connectStart);
	        Response=TimeChange(Timeline.responseEnd-Timeline.responseStart);
	        Request=TimeChange(Timeline.responseStart-Timeline.requestStart);
	        Blank=TimeChange(Timeline.domInteractive-Timeline.responseStart);
	        domContentLoaded=TimeChange(Timeline.domContentLoadedEventEnd-Timeline.navigationStart);
	        Onload=TimeChange(Timeline.loadEventEnd-Timeline.navigationStart);
	        console.log('Dns:'+Dns+' Connect:'+Connect+' Request:'+Request+' Response:'+Response+' Blank:'+Blank+' domContentLoaded:'+domContentLoaded+' Onload:'+Onload);
	    }
	})();
