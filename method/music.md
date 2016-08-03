# 音乐功能

当满足以下条件，音乐会自动播放。

-   启用了 music 插件。
-   音乐开关已经开启，可通过 yp.settings.switch_music 查看值为 true (开启) 或者 false (关闭)。
-   有数据传入，前文配置中有提到数据格式。


    data:[{
            title: "Danger in Loving You",
            url: "http://image2.panocooker.com/group1/M00/99/D7/rBELCleJWfCAUO7LADidTCzAs68072.mp3|http://image2.panocooker.com/group1/M00/99/DB/rBELC1eJWfGAFuRnAhgRhnvuGZ0885.wav|http://image2.panocooker.com/group1/M00/99/DB/rBELC1eJWfGAGpdBACSoWK6zViY341.ogg"
        }
    ]



可以传入多首音乐，插件会根据传入顺序依次循环播放。多种音乐格式用 " | " 隔开，主要是为了兼容不同的浏览器。

音乐提供以下方法：

方法名 | 类型 | 参数 |  作用
-----|------|----|----
pause | Function | 无 |暂停/播放音乐
play | Function | Array |  播放音乐
stopMusic | Function | 无 |  停止播放所有音乐
xml | String | "plugins/xml/music.xml" |  导入依赖的xml文件

调用示例

    yp.method.music.play([{url:"http://image2.panocooker.com/group1/M00/99/D7/rBELCleJWfCAUO7LADidTCzAs68072.mp3"}])
