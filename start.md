# 开启一个新的全景

##### 开启一个新的全景，必须引入以下文件

    <script type="text/javascript" src="http://code.panocooker.com/v1.1/depend/jquery/jquery.min.js"></script> // 全站依赖jquery.js
    <script type="text/javascript" src="http://code.panocooker.com/v1.1/depend/layer/layer.js"></script> // 所有的弹窗依赖layer.js
    <script type="text/javascript" src="http://code.panocooker.com/v1.1/depend/switch/lc_switch.js"></script> //模拟ios切换表单，没用到可以不引用
    <script type="text/javascript" src="http://code.panocooker.com/v1.1/depend/iscroll/iscroll.js"></script> // 所有的插件中滚动条都是用iscroll.js实现
    <script type="text/javascript" src="http://code.panocooker.com/v1.1/main.all.js"></script> // 封装krpano用到的主要文件,必须引用


main.js 暴露一个 YP 的全局构造函数，实例化YP，即可打开一个全景, 如无特别说明，后面出现的小写yp即为实例化的全景。

    var yp = new YP({
        panoId: 46672,     // 云曈数据库中的pano ID。 
        data: {            // 配置数据，可以相关插件中写入数据。
            group:true,    // 全景导航与分组 
            maps:true,     // 平面地图，可添加雷达
            hotspots: true,// 热点
            nadir:true,    // 补天与补地图片
            switcher:true, // 开关插件 
            music:true,    // 音乐
            effect: true,  // 特效
            toolbar:true,  // 开启工具栏，可通过skin配置来调用文件
            webvr:true,    // web VR
            comments: true,// 热点评论
            links:true,    // 热点连接器
            count:true,    // 点赞功能
            share: true    // 微信分享
        },
        callback: {}       // 回调函数
    });

yp中插件属性的值为以下四种，

- ture 表示调用云曈默认数据
- false 表示不调用数据，但插件仍会初始化。
- {} 启用插件并且有自定义数据
- "string" 表示重命名请求数据,如：link:"links",表示请求links数据，初始化link插件。一般我们在设计时是对应上的。

我们可以在浏览中输入以下网址可以直观的看到请求到的数据。

    http://pano.panocooker.com/getSomething?id=46672&something=group,maps,hotspots,nadir,switcher,music,effect,toolbar,webvr,comments,links,count

yp绑定了以下重要的方法和属性，可以在浏览器调试模式下查看。

- krpano  获取到krpano对象。
- settings 当前场景的相关设置
- method    所有的方法
- plugin    所有的插件 
- events    所有的事件
- element   全景dom对象

