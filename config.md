# 关于配置

封装的配置项都是基于jquery的extend方法实现,实现代码如下：

    options = $.extend(true, {},DEFAULT_OPTION, option);


在本项目中，yp中的配置会覆盖skin中的配置，然后再覆盖插件中的默认配置。

    this.option = $.extend(true, {}, yp.DEFAULT_OPTION, this.skin, option);

配置选项如下：

    panoId: undefined,
    passQueryParameters: false,
    id: "krpanoSWFObject",
    target: "pano" + new Date().getTime(),              // krpano要放入的容器中
    vars: {},   
    skin: "default",                                    // UI 设置
    swf: codePath + "/krpano/krpano.swf",
    xml: undefined,                                     // 要加载的xml文件
    mwheel: true,                                       // 是否启用鼠标中键
    initvars: {
        STATIC: codePath + "/static/",                  // XML中用到的图片文件存放目录
        CODEURL: codePath,                              // 静态文件存放目录
        PANOCOOKERURL: "http://pano.panocooker.com"     // 全景根目录
    },
    path: "http://pano.panocooker.com",
    width: "100%",
    height: "100%",
    callback: { }

