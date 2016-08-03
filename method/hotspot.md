# 热点插件

图文热点、热点评论、热点连接器是基于krpano的热点的三种形态。前文配置中提到的数据格式都有热点的坐标和样式。

    ath: "47.915554824184596",
    atv: "-12.957931474987838",
    style: 102,

只是三者携带的数据略有差异。链接器必须有指向的场景名，评论必须有头像和评论内容，图文热点必须有标题、内容、图片、链接地址等。

对于不同形态的热点，先通过注册生成一个类。如连接器：

    var links = yp.method.hotspot.register("links",{});

这个方法体有两个参数，一个是类名，一个是传初始化数据，可以为空。类有这个方法体：

方法名 |  参数 |  作用
-----|----|----
addHotspot | { style: 101,data: {} } | 添加热点，右侧参数为添加连接器默认的参数。
getHotspot  | name |  获取热点，参数为热点名字
init | 无 |  处理实列化类时传递过来的数据——生成热点


##### Hotspot的方法体

方法名 |  参数 |  作用
-----|----|----
getData | 无 | 获取当前热点数据
remove | 无 | 移除当前热点
save | Object data | 保存热点数据
setMove | Boolean true / false |  是否移动
update | Object data | 更新热点 
zorder | Boolean true / false | 设置热点层级，true为提升层级，不会被别的热点遮挡


##### Hotspot的默认设置项

属性 |  属性值 |  作用
-----|----|----
align | "center" | 热点对齐方式
callback | {}  | 回调函数，下文专门介绍
data  | undefined |  热点数据，默认为空数组
hotspotType | 无  | 热点类型
isMove | true | 可以移动
style | "spotgif1" | 默认样式
x | 0 | 设置热点偏移x值
y | 0 | 设置热点偏移y值


##### Hotspot的`callback`项

回调方法名 | 触发条件
-----| ----
onLoaded |  热点加载完成触发
onAddHotspot | 添加热点触发
onClick |  鼠标点击触发
onOver |  鼠标移入触发
onOut |  鼠标移出触发
onHover |  鼠标移上触发
onDown |  鼠标按下触发
onUp |  鼠标弹起触发 



