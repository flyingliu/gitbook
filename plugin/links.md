# 热点连接器

连接器方法体

方法名 |  参数 |  作用
-----|----|----
addLink | obj | 添加一个连接器热点
getLink | name | 根据名字获取连接器
removeLink  | hotspot | 删除传入热点
saveHotspot | 无 | 保存当前热点
toggleLink | true/false | 显示/隐藏连接器
init | obj | 初始化连接器
onNewSceneCacheData | 无 | 缓存当前场景的链接器
onNewSceneData | obj | 获取新场景的连接器数据

调用例子：

    yp.plugin.links.addLink()

添加了一个新的链接器热点