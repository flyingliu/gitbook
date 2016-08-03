# UI配置与换肤

#####  更换图文热点、评论样式

功能与插件中用到的样式都打包在 `/v1.1/static/css/plugin.all.css` 中，可以重写样式来覆盖以前的样式。

#####  更换导航菜单、logo、点赞等

导航菜单、logo、点赞等内容是分离于krpano并覆盖其上的。通常的dom结构如下图：

![](//flyingliu1.gitbooks.io/gitbook/content/images/dom.png)

这部分内容我们可以单独引用独立的CSS，JS文件来改变其内容与界面。

- 首页，在 yp 中配置 skin 的值，可参考[关于插件的配置](config/plugin_config.md)。如：`skin: "store"`，skin的属性值与skinConfig中的配置项`store` 是要对应上的，否则无法加载到文件。
- 在 `main.all.js` 有预设要调用的CSS和JS文件。


    var skinConfig = {
        store:{
            js: "./skin/store/store.all.js",
            css: "./skin/store/css/toolbar.css"
        },
        default: {
            ...
        }
    }


- CSS和JS文件会以ajax同步的形式插入到**页面头部**。

    ![](//flyingliu1.gitbooks.io/gitbook/content/images/style.png)

    这里要注意的是文件路径，css、js是相当于直接写在页面上的，如果资源文件路径是相对路径，要写相对于当前页面的路径，而不是相对于CSS的引入路径，所以CSS中引入资源（图片地址）最好是绝对路径。
    
- 我们在`duc.common.js`文件中定义了一个loadSkin的全局函数，该函数会以同步ajax的形式加载css和js文件。由于在项目中我们没有用seajs、Loadjs、requirejs等文件加载器，如果用加载器加载文件可能有些地方会报错。


