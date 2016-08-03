# 补天补地

###### 补天补地的方法

方法名 |  参数 |  作用
-----|----|----
get | 无 | 获取补天补地数据
set | String pic,String  url, Boolean skyFlag | 设置补天补地，pic为图片地址；url为转地址；skyFlag为true表示设置补天，false表示设置补地
swith | Boolean flag,Boolean skyFlag | 显示/隐藏补天补地，flag为true表示显示，false隐藏，skyFlag为true表示补天，false表示补地
resize | Boolean skyFlag | 重置补天补地图片，skyFlag为true表示补天，false表示补地
xml | String "/krpano/skin/plugin/nadirlogo.xml" | 导入依赖的xml文件

调用例子：
    yp.method.nadir.swith(false,false)

隐藏补地图片。 
