# 场景

方法名 |  参数 |  作用
-----|----|----
addScene | String scene | 添加场景
callwith | String type, Object data | 传递回调事件
getCurrScene | 无 | 获取当前场景
getScene | String name | 获取场景列表
setData | Array data | 设置数据
loadScene | String name | 加载场景
removeScene | String scene | 删除场景
setData | String name | 获取场景列表


场景 callback 函数

方法名 |  触发条件
-----|----
onSceneAdd | 添加场景触发方法
onSceneRemove | 移除场景触发 

调用示例：

    yp.method.scene.loadScene("imilhf0c")

加载name为`imilhf0c`的场景


