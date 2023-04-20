取得熱門文章列表
==============
*   [Request](#request)
*   [Parameter](#parameter)
*   [Response](#response)

<h2 id="request">Request</h2>

*   method: Post
*   host: https://forum-server.batmobile.com.tw/
*   path: api/v1/article/getHotList/all

<h2 id="parameter">Parameter</h2>

```json
{
	"pageSize": Int, //一次要取得幾篇文章
	"excludeArticleIds": [String] //上一次請求時得到的熱門文章id列表，在請求下一批熱門文章時用來排除已經查詢過的熱門文章。 ex.第一次請求時帶空陣列[]因為還沒有前一次的請求，Api回傳了"excludeArticleIds": ["a", "b", "c"]，第二次需要加載更多文章時需帶入"excludeArticleIds": ["a", "b", "c"]
}

//Example:
{
	"pageSize": 10,
	"excludeArticleIds": []
}
```

<h2 id="response">Response</h2>

```json
{
    "result": [
		{
			"title": String, //文章標題
			"content": String, //文章內容
			"createdAt": String, //發文時間
			"authorAvatarUrl": String, //作者頭像
			"authorAlias": String //作者名稱
		}
	],
	"excludeArticleIds":[String] //下次請求時需排除的熱門文章id
}

//Exapmle:
{
	"result": [
		{
			"title": "Anonymous test",
			"content": "Tony Anonymous",
			"createdAt": "2022-11-08T04:29:19.786Z",
			"authorAvatarUrl": "https://foootball.cc/uploads/users/kU2jR5Dllh.png",
			"authorAlias": "訪客1"
		},
		{
			"title": "Anonymous test1",
			"content": "Zoe Anonymous",
			"createdAt": "2023-01-09T09:57:10.646Z",
			"authorAvatarUrl": "1234",
			"authorAlias": "訪客2"
		},
		{
			"title": "Anonymous test2",
			"content": "Kai Anonymous",
			"createdAt": "2022-09-27T20:10:52.613Z",
			"authorAvatarUrl": "https://i.imgur.com/draWwIB.jpg",
			"authorAlias": "訪客"
		}
	],
	"excludeArticleIds": [
		"6369db1ffa1670066bee2bf3",
		"63bbe43fae90601a9dd0c21e",
		"63bbe4f6ae90601a9dd0c3ea"
	]
}
```