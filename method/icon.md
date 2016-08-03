# 热点样式

方法名 |  参数 |  作用
-----|----|----
get | String url | 获取样式列表，传入url,会根据url查询匹配的样式对象
getIcon | String name | 根据名字查询匹配的样式对象
getStyle | Number iconid | 根据样式Id查询匹配的样式对象
getIconPackage | 无 | 获取样式分组对象包

调用例子：

    yp.method.icon.get("http://image2.panocooker.com/group1/M00/53/45/rBELC1eE3JKACTuBAAAEayC8gz0592.png");
    yp.method.icon.getStyle(101);


