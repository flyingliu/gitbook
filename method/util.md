# 公用方法

方法名 |  参数 |  作用
-----|----|----
browser | 无  | 检测浏览器类型
createItem | addName, name |
hasTouch | 无  | 返回触摸屏的点击事件，非触摸屏为 `click`
include | String url | 加载 xml 文件
isTouch | 无  | 判断是否为触摸屏
loading | 无  | 返货 longing 的 dom
replaceUrl | String url | 替换krpano中的路径
strLength | String str | 获取字符串的长度，一个中文字符当作两个半角字符长度
switchAutorotate | Boolean flag | 全景自动旋转开关

调用示例：

    yp.method.util.strLength("abc北京天安门")  // 13

获取字符串的长度
