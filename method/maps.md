# 平面地图

通过注册获取maps

    maps = yp.method.maps.register("maps", options);

###### maps的方法体

方法名 |  参数 |  作用
-----|----|----
_getNotUseScene | String name | 获取没有雷达使用的场景
activeByScene | 无 |  通过场景切换激活雷达 
activeMap | Maps map | 激活地图
addMap | Object data | 添加地图
addRadar | Boolean flag,Object data | 添加雷达
callwith | String type,Object  data | 回调传递，执行插件默认的回调事件，再执行配置选项中的回调函数 
createdMap | 无 | 创建地图
getMaps | 无 | 获取地图
getPlugin | String name | 获取krpano中的plugin。
init | Object  options,Object funs | 初始化地图方法，funs为传递krpano、setting、method、plugin等对象。
initData | Number i | 初始化地图数据
removeMap | Maps map | 删除地图
removeRadar | 无 | 删除雷达
resize | Number width,Number height | 适配地图，参数传入宽高。
unActiveMap | 无 | 取消选中地图

调用例子：

    yp.plugin.maps.maps.resize(100,100)