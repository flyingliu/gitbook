# 开关插件

###### 开关插件方法体：

方法名 |  参数 |  作用
-----|----|----
getSwitch | 无 | 获取开关数据
init | 无 | 初始化开关插件
onNewSceneData | data | 加载新场景更新数据
switchOff | name,type | 设置开关，传入开关名和值


开关名 |  值
-----|----
hotspot | Boolean value
gyro | Boolean value
music | Boolean value
starview | Boolean value 
autorotate | Boolean value 
comment | Boolean value

调用例子：

    yp.plugin.switcher.switchOff("music",false)

暂停音乐播放


