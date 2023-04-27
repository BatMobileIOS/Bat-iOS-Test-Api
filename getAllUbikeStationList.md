取得所有UBike站點
==============
*   [Request](#request)
*   [Response](#response)

<h2 id="request">Request</h2>

*   method: Get
*   url: https://tcgbusfs.blob.core.windows.net/dotapp/youbike/v2/youbike_immediate.json

<h2 id="response">Response</h2>

```json
[
    {
        "sno": String, //站點編號
        "sna": String, //站點名稱
        "tot": Int, //站點總停車格數
        "sbi": Int, //目前車輛數
        "sarea": String, //行政區 ex.大安區、中山區
        "mday": String, //微笑單車各場站來源資料更新時間
        "lat": Double, //緯度
        "lng": Double, //經度
        "ar": String, //地址
        "sareaen": String, //英文行政區 ex.大安區、中山區
        "snaen": String, //英文站點名稱
        "aren": String, //英文地址
        "bemp": Int, //空位數量
        "act": String, //站點目前是否禁用 ex."0"禁用中, "1"啟用中
        "srcUpdateTime": String, //微笑單車系統發布資料更新的時間
        "updateTime": String, //北市府交通局數據平台經過處理後將資料存入DB的時間
        "infoTime": String, //微笑單車各場站來源資料更新時間
        "infoDate": String //微笑單車各場站來源資料更新時間
    }
]

//Exapmle:
[
    {
        "sno": "500101001",
        "sna": "YouBike2.0_捷運科技大樓站",
        "tot": 28,
        "sbi": 0,
        "sarea": "大安區",
        "mday": "2023-04-27 14:41:14",
        "lat": 25.02605,
        "lng": 121.5436,
        "ar": "復興南路二段235號前",
        "sareaen": "Daan Dist.",
        "snaen": "YouBike2.0_MRT Technology Bldg. Sta.",
        "aren": "No.235， Sec. 2， Fuxing S. Rd.",
        "bemp": 28,
        "act": "1",
        "srcUpdateTime": "2023-04-27 14:41:28",
        "updateTime": "2023-04-27 14:41:52",
        "infoTime": "2023-04-27 14:41:14",
        "infoDate": "2023-04-27"
    },
	{
        "sno": "500101002",
        "sna": "YouBike2.0_復興南路二段273號前",
        "tot": 21,
        "sbi": 0,
        "sarea": "大安區",
        "mday": "2023-04-27 14:21:04",
        "lat": 25.02565,
        "lng": 121.54357,
        "ar": "復興南路二段273號西側",
        "sareaen": "Daan Dist.",
        "snaen": "YouBike2.0_No.273， Sec. 2， Fuxing S. Rd.",
        "aren": "No.273， Sec. 2， Fuxing S. Rd. (West)",
        "bemp": 21,
        "act": "1",
        "srcUpdateTime": "2023-04-27 14:41:28",
        "updateTime": "2023-04-27 14:41:52",
        "infoTime": "2023-04-27 14:21:04",
        "infoDate": "2023-04-27"
    },
    {
        "sno": "500101003",
        "sna": "YouBike2.0_國北教大實小東側門",
        "tot": 16,
        "sbi": 0,
        "sarea": "大安區",
        "mday": "2023-04-27 14:35:04",
        "lat": 25.02429,
        "lng": 121.54124,
        "ar": "和平東路二段96巷7號",
        "sareaen": "Daan Dist.",
        "snaen": "YouBike2.0_NTUE Experiment Elementary School (East)",
        "aren": "No. 7， Ln. 96， Sec. 2， Heping E. Rd",
        "bemp": 16,
        "act": "1",
        "srcUpdateTime": "2023-04-27 14:41:28",
        "updateTime": "2023-04-27 14:41:52",
        "infoTime": "2023-04-27 14:35:04",
        "infoDate": "2023-04-27"
    },
    {
        "sno": "500101004",
        "sna": "YouBike2.0_和平公園東側",
        "tot": 11,
        "sbi": 0,
        "sarea": "大安區",
        "mday": "2023-04-27 14:41:14",
        "lat": 25.02351,
        "lng": 121.54282,
        "ar": "和平東路二段118巷33號",
        "sareaen": "Daan Dist.",
        "snaen": "YouBike2.0_Heping Park (East)",
        "aren": "No. 33， Ln. 118， Sec. 2， Heping E. Rd",
        "bemp": 11,
        "act": "1",
        "srcUpdateTime": "2023-04-27 14:41:28",
        "updateTime": "2023-04-27 14:41:52",
        "infoTime": "2023-04-27 14:41:14",
        "infoDate": "2023-04-27"
    }
]
```