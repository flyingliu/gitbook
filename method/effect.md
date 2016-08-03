# 特效

###### 特效的方法

方法名 |  参数 |  作用
-----|----|----
get | 无 | 获取特效数据
set | Object effectObj,Number size| 设置特效，effectObj为特效基本参数，size为特效速率，1:小,2:中,3大
switch | Boolean flag | 显示/隐藏特效，flag为true表示显示，false隐藏
initPlugin | 无 | 初始化特效功能，默认特效隐藏


调用例子：

    var effectObj = {
        mode: "rain",
        imageurl: "",
        imagescale: "1",
        flakes: "1500",
        color: "0xFFFFFF",
        floor: "0.7",
        speed: "1.0",
        spreading: "1",
        shake: "4.0",
        speedvariance: "2.0",
        wind: "3",isUse:true,
        winddir: "0",
        rainwidth: "1",
        rainalpha: "1",
        visible: true
    }
    yp.method.effect.set(effectObj,3);
    yp.method.effect.switch(true);


设置特效，默认的特效是隐藏的，显示特效即可看到效果。 
