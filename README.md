# lazy-load
图片懒加载
例子见[DEMO](http://www.lovewebgames.com/jsmodule/lazy-load.html)  
![预览效果:](/example/lazy-load.gif "点击预览效果")
#使用方法案例:
    <img data-src="http://ott.wansecheng.com/weidian/wdgoods/1429250625186.jpg" alt="">
    $('img').LazyLoad({
        container: window,
        effect: 'show',
        effectArgs: 'slow',
        loadImg:'loading.gif',
        load: null,
        offset: 0
    });
#或者
    var obj = new LazyLoad();
    obj.init({
        elements:'img',
        container: window,
        effect: 'show',
        effectArgs: 'slow',
        loadImg:'loading.gif',
        load: null,
        offset: 0
    });
***
#属性和方法
##elements:
    dom的集合，一般为需要懒加载的img标签集合，如果是动态加载的内容，请在html加载完成之后再调用init
##init:
    初始化方法
##container:   window
    触发滚动条的容器，默认为window,可不传
##event:  "scroll"
    容器触发事件，默认为scroll
##effect:
    触发的事件方法，默认为 show
##effectArgs
    要给effect传的参数，可不传
##loadImg
    加载等待时显示的图片地址，默认是一个1pxx1px的图
##offset:
    与图片的差值，默认0
##load:function(img)
    加载完成的回调,this指向当前对象
