# 地图插件

地图插件提供了平面地图加雷达的功能。一个地图上可以有多个雷达点。一个雷达点对应一个全景。地图编辑状态下提供了雷达的增删改。

    option: {
        move: false,                // 设置地图是否可以移动，在编辑状态下可以设置为true
        radar: {                    // 设置雷达角度是否可以编辑
            editHeading: false
        },
        style: {                    // 设置地图默认状态
            width: 262,
            height: 200,
            bgAlpha: 0,
            bgColor: 0xffffff
        },
    }

    data: [{
        id: 283,
        name: "map_2.jpg",          // 地图名字
        url: "...",                 // 地图背景图片
        radars: [{                  // 雷达
            id: 950,
            scene: "igij6pep",
            x: 355,
            y: 525,
            heading: "108.0"
        }]
    }]



###### 地图插件封装的方法有：

方法名 |  参数 |  作用
-----|----|----
addMap | 无 | 添加地图
callwith | String type, Object data | 回调传递，执行插件默认的回调事件，再执行配置选项中的回调函数 
getCurrMap | 无 | 获取当前地图
getMaps | 无 | 获取地图
init | Object data | 初始化插件
onaddscene | 无 | 添加场景触发方法
onnewscene | 无 | 加载场景触发方法
onremovescene | 无 | 移除场景触发方法
removeMap | Maps map | 删除地图


##### maps的`callback`项

回调方法名 | 触发条件
-----| ----
onMapsAdd |  添加地图时触发
onRadarAdd | 添加雷达时触发
onRadarRemove |  移除雷达时触发
onRadarChange |  改变选中雷达时触发


调用例子：

    yp.plugin.maps.addMap({url:"http://image2.panocooker.com/group1/M00/9E/AB/rBELCleVpryAUknyAABYAIyWf_0954.png",name:"mapa"})








