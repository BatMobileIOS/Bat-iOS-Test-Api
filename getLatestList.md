取得最新文章列表
==============
*   [Request](#request)
*   [Parameter](#parameter)
*   [Response](#response)

<h2 id="request">Request</h2>

*   method: Post
*   host: https://forum-server.batmobile.com.tw/
*   path: api/v1/article/getLatestList/all

<h2 id="parameter">Parameter</h2>

```json
{
    "page": Int, //第幾頁。從0開始
    "pageSize": Int, //一次取幾篇文章
    "lastId": String //上一次請求時回應的lastId。ex.請求第0頁時回傳"lastId": "AAA"，下一次請求第1頁時就要帶入"lastId": "AAA"。請求第一頁時帶入空字串即可
}

//Example: 請求第一頁時所戴的參數(以10篇文章為例)
{
    "page": 0,
    "pageSize": 10,
    "lastId": ""
}
```

<h2 id="response">Response</h2>

```json
{
    "result": [ //回傳的文章列表
        {
	     "title": String, //文章標題
	     "content": String, //文章內容
	     "createdAt": String, //發文時間
	     "authorAvatarUrl": String, //作者頭像
             "authorAlias": String //作者名稱
        }
    ],
    "lastId": String //下次請求其他分頁時需帶入請求中
}

//Exapmle:
{
     "result": [
     	{
	     "title": "Anonymous test",
	     "content": "Tony Anonymous",
	     "createdAt": "2022-11-08T04:29:19.786Z",
	     "authorAvatarUrl": "https://foootball.cc/uploads/users/kU2jR5Dllh.png",
	     "authorAlias": "Z test1"
	},
	{
	     "title": "Anonymous test1",
	     "content": "Zoe Anonymous",
	     "createdAt": "2023-01-09T09:57:10.646Z",
	     "authorAvatarUrl": "1234",
	     "authorAlias": "shawn test1"
	},
	{
	     "title": "Anonymous test2",
	     "content": "Kai Anonymous",
	     "createdAt": "2022-09-27T20:10:52.613Z",
	     "authorAvatarUrl": "https://i.imgur.com/draWwIB.jpg",
	     "authorAlias": "shawn test1"
	}
    ],
    "lastId": "6369db1ffa1670066bee2bf3"
}
```
