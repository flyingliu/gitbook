# 配置分组与导航


yp 中的group 数据格式

    group: {
        data:[{
            name: "默认组",
            groupId: 6654,
            list: [{
                id: 46673,
                name: "xq7ui241",
                title: "3",
                thumb: "http://image2.panocooker.com/group1/M00/99/18/rBELCleHNZiASEQBAAAXOI1V0iQ505.jpg",
                xml: "http://pano.panocooker.com/getXml2?id=46673&mainId=46672"
            }]
        },
        ...
        ]
    },

yp 中的music 数据格式

    music: {
        data:[{
            title: "Danger in Loving You",
            singer: "Halie Loren",
            album: "Stages",
            mins: "00:03:19",
            url: "http://image2.panocooker.com/group1/M00/99/D7/rBELCleJWfCAUO7LADidTCzAs68072.mp3|http://image2.panocooker.com/group1/M00/99/DB/rBELC1eJWfGAFuRnAhgRhnvuGZ0885.wav|http://image2.panocooker.com/group1/M00/99/DB/rBELC1eJWfGAGpdBACSoWK6zViY341.ogg"
        },
        ...
        ]
    }

yp 中的switcher 数据格式

    switcher: {
        data: {
            hotspot: 1,     //热点开关
            gyro: 1,        //陀螺仪
            comment: 1,     //评论开关
            music: 1,       //音乐
            starview: 1,    //小行星
            autorotate: 1   //自动旋转
        }
    },

yp 中的switcher 数据格式

    switcher: {
        data: {
            hotspot: 1,     //热点开关
            gyro: 1,        //陀螺仪
            comment: 1,     //评论开关
            music: 1,       //音乐
            starview: 1,    //小行星
            autorotate: 1   //自动旋转
        }
    },

yp 中的comments 数据格式

    comments: {
        data:[{
            ath: "126.11392690004028",
            atv: "0",
            data: {
                avatar: "http://static.duc.cn/yunsj/2015/12/30/35399177.png",
                content: "这里是评论内容",
                hotspotId: 46308,
                createdId: 90028
            }
        },
        ...
        ]
    }

yp 中的links 数据格式

    links: {
        data:[{
            ath: "77.09530509550984",
            atv: "20.3533847515102",
            style: 101,
            data: {
                hotspotId: 46989,
                sceneId: 38530,
                sceneName: "igij6pep",
                createdId: 90028
            }
        },
        ...

        ]
    }
 
yp 中的hotspos 数据格式

    hotspots: {
        data:[{
            ath: "47.915554824184596",
            atv: "-12.957931474987838",
            style: 102,
            data: {
                hotspotId: 46990,
                type: 1,
                linkUrl: "http://www.yuntongzi.com",
                thumb: "",
                title: "标题",
                content: "内容",
                pic: [
                    "/group1/M00/9E/AB/rBELCleVplSAFEAsAAIEAGAPIBo019.png",
                    "/group1/M00/9E/AE/rBELC1eVplSAQ0ClAAJkAEEdTYA728.png"
                ],
                createdId: 90028
            }
        },
        ...

        ]
    }

yp 中的maps 数据格式

    maps: {
        data: [{
            id: 283,
            name: "map_2.jpg",
            url: "http://image2.panocooker.com/group1/M00/9E/AB/rBELCleVpnKAYb2RAAFwAHEUdZo050.jpg",
            radars: [{
                id: 950,
                scene: "igij6pep",
                x: 355,
                y: 525,
                heading: "108.0"
            },
            ...
            ]
        },
        ...
        ]
    }


yp 中的effect 数据格式

    effect: {
        data:{
            id: 3,
            mode: "image",
            imageurl: "http://image2.panocooker.com/group1/M00/48/A3/rBELC1eE1cKAAFAzAAAHe_2ApLQ014.png",
            imagescale: "0.5",
            flakes: "200",
            color: "0xFFFFFF",
            floor: "0.7",
            speed: "1.5",
            spreading: "1",
            shake: "1",
            speedvariance: "2",
            wind: "0.0",
            winddir: "0",
            rainwidth: "0.5",
            rainalpha: "0.5",
            type: 0,
            isdefault: true,
            isall: false,
            isuse: true
        }
    }
 
其他需要调用但是不需要传数据的插件，直接在插件名称后面赋值为 ture,如：

    toolbar: true

相应的如果停用该插件，只需赋值为 false 。

补天与补地图片，数据是直接从XML文件中获取的，所以只能在输出的XML中更改数据。
