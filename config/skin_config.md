# UI配置

在实例化yp中可以设置 skin 字段，默认的 skin 是 "default", 在瞳掌柜页面可以设置：
    
    skin: "store"

然后就可以配置各插件的值和重新定义回调等。通常在插件中有以下值是可以定义的。
    
    template: ""    // 如果在页面有显示内容的，通常可以通过这个重写模板
    element: ""     // 要插入到的dom中，比如：$("body")
    callback: ""    // 插件的回调
    data:           // 插件数据

    move：ture      // 与热点相关的通常有这个配置
    radar:          // 雷达
    style:          // 地图样式


我们可以通过重新定义回调来合并与请求数据。

    YP.addSkin("store", {
        plugin: {
            maps: {
                // element:$(".map"),
                move: false,
                radar: {
                    editHeading: false
                },
                style: {
                    width: 262,
                    height: 200,
                    bgAlpha: 0,
                    bgColor: 0xffffff
                },
                template:"<div class='maps-bg'>\
                        <div class='maps-tab'>\
                            <ul class='maps-names'>\
                            </ul>\
                        </div>\
                        <div class='getMapsHeight'/>\
                        <div class='maps'/>\
                        <div class='sceneWrap' />\
                    </div>"
            },
            ...
        },
        callback: {
            onLoadData: function (something, fn) {
                var _this = this;
                this.proxy.getSomething({
                    id: this.method.scene.getCurrScene().id,
                    mainId: this.option.panoId,
                    something: something
                }, function (data) {
                    if(data.success){
                        _this.proxy.getAppSomething({
                            userId: getQueryString("userId")
                        }, function (appData) {
                            if(appData.success){
                                var newData = $.extend(true, {}, data.data, appData.data);
                                fn(newData);
                            } else {
                               YP.error(appData.errMsg); 
                            }
                        })
                    } else {
                        YP.error(data.errMsg);
                    }
                })
            },
            ...
        }
    });
