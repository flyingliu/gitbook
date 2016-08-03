# 图文热点插件

图文热点方法体

方法名 |  参数 |  作用
-----|----|----
addHotspot | obj | 添加一个图文热点
getHotspot | name | 根据名字获取图文热点
removeHotspot  | hotspot | 删除传入图文热点
saveHotspot | obj | 保存热点
switch | true/false | 显示/隐藏图文热点
init | obj | 初始化图文热点
updataHotspot | iconId,packageId,hotspot | 更新图文热点
onNewSceneCacheData | 无 | 缓存当前场景的图文热点
onNewSceneData | obj | 获取新场景的图文热点数据

调用例子：

    yp.plugin.hotspots.addHotspot()

添加了一个新的图文热点

##### 图文热点的默认配置项

属性 |  属性值 |  作用
-----|----|----
callback | obj | 回调，参考热点回调
data | undefined | 默认数据
isEdit | fasle | 是否编辑状态
isMove | false | 热点是否可移动
style | 102 | 默认样式Id
template | dom | 初始化的dom


