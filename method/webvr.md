# VR

方法名 |  参数 |  作用
-----|----|----
exitVr | 无 | 退出VR
enterVr | 无 | 进入VR
init | 无 | 初始化VR方法
on | String type, Function fun | 绑定进入/退出VR的事件,tpye 为 `exitvr` 表示退出，`entervr` 为进入
remove | String type, Function fun | 解绑进入/退出VR的事件,tpye 为 `exitvr` 表示退出，`entervr` 为进入
onnewpano | String name | VR模式下进入新场景方法


调用示例：

    yp.method.webvr.enterVr()

全景进入VR模式

