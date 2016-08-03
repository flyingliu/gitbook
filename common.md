# 常用函数与方法

##### 使用模板

项目中默认引入了[template.js](https://github.com/yanhaijing/template.js),这个是一个性能单一小巧灵活的处理简单模板的js库。具体使用方法可以参考[template.js帮助文档](https://github.com/yanhaijing/template.js)

##### 与服务器的交互
在YP全局对象上绑定了一个proxy方法，可以在浏览器调试模式下输入 `YP.proxy` 查看所有的方法体。其中交互的地址可以通过 `window.PROXY_URL` 的全局变量进行覆盖。

方法名 | 参数 | 作用
-----|------|----
ajax | Object op | 封装了jquery 的 ajax 方法，带有token信息
get | Object op, Function success, Function error, Boolean  async | 简化的ajax方法，get方式访问
post | Object op, Function success, Function error, Boolean  async |  简化的ajax方法，post方式访问
updateDate | Object options | 设置token信息
addUrl | name, url | 遍历YP.url 对象，只需定义一个url,就会生成一个相应的方法体。


##### bug调试
项目中默认引入了logger.js文件，封装了console的一些方法。可以直接在浏览器调试模式下输入 `logger`,可看到方法体。

方法名 | 参数 | 作用
-----|------|----
debug | value, error | value为要输出的值，同consle.debug(value)
info | value, error | value为要输出的值，同consle.info(value)
levels | 无 | 错误提示等级  {debug: 1, log: 2, info: 3, warn: 4, error: 5}
log | value, error | value为要输出 的值，同consle.log(value)
setThresholdInt | String level | 设置错误输出等级。 level的值为“debug / info / log / warn / error”
warn | value, error | value为要输出的值，同consle.warn(value)


默认为debug等级，调试中 输入 ： `logger.log("a")`,可看到有 a 输出。然后设置调试等级为 `error`.
    
    logger.setThresholdInt("error")

再输入 `logger.log("a")`，可看到没有输出。在生成环境可提高输出等级。



##### 其他公用函数
函数名 | 参数 | 作用
-----|------|----
getQueryString | String name, String url |  获取url参数
changeURLPar | String ref, String value, String url | 设置url参数值，ref参数名,value新的参数值 
jsonToStr | Object json | 对象转化为json字符串
checkStr | String str | 判断特殊字符
updateUrl | String url, String title | 设置url,更新文档 title
loadSkin | String id, String url,Boolean type | 加载静态资源 css 和 js文件，type == ture 为css文件, false 时是js文件
previewImage | file, img | file 上传图片控件对象,img 需要展示的img对象



----
##### 参考资料

- [template.js帮助文档](https://github.com/yanhaijing/template.js)