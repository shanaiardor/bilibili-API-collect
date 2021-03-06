# 统计与数据

本页所有操作均需登录（SESSDATA）

统计与数据次日中午12刷新

## UP主视频状态数据

> http://member.bilibili.com/x/web/index/stat

*方式：GET*

**json回复：**

| 字段    | 类型 | 内容     | 备注         |
| ------- | ---- | -------- | ------------ |
| code    | num  | 返回值   | 0：成功      |
| message | str  | 错误信息 | 默认为0      |
| ttl     | num  | 1        | 作用尚不明确 |
| data    | obj  | 信息本体 |              |

`data`对象：

| 字段              | 类型 | 内容           | 备注 |
| ----------------- | ---- | -------------- | ---- |
| fan_recent_thirty | obj  | 粉丝数变化情况 |      |
| inc_coin          | num  | 新增投币数     |      |
| inc_elec          | num  | 新增充电数     |      |
| inc_fav           | num  | 新增收藏数     |      |
| inc_like          | num  | 新增点赞数     |      |
| inc_share         | num  | 新增分享数     |      |
| incr_click        | num  | 新增播放数     |      |
| incr_dm           | num  | 新增弹幕数     |      |
| incr_fans         | num  | 新增粉丝数     |      |
| incr_reply        | num  | 新增评论数     |      |
| total_click       | num  | 总计播放数     |      |
| total_coin        | num  | 总计投币数     |      |
| total_dm          | num  | 总计弹幕数     |      |
| total_elec        | num  | 总计充电数     |      |
| total_fans        | num  | 总计粉丝数     |      |
| total_fav         | num  | 总计收藏数     |      |
| total_like        | num  | 总计点赞数     |      |
| total_reply       | num  | 总计评论数     |      |
| total_share       | num  | 总计分享数     |      |

`data`中的`fan_recent_thirty`对象：

| 字段     | 类型 | 内容     | 备注 |
| -------- | ---- | -------- | ---- |
| follow   | obj  | 涨粉情况 |      |
| unfollow | obj  | 掉粉情况 |      |

`fan_recent_thirty`中的`follow`对象：

| 字段         | 类型 | 内容   | 备注             |
| ------------ | ---- | ------ | ---------------- |
| ｛YYYYMMDD｝ | num  | 涨粉数 | 字段名为日期     |
| ……           | num  | ……     | 近30天的涨粉情况 |

`fan_recent_thirty`中的`unfollow`对象：

| 字段         | 类型 | 内容   | 备注             |
| ------------ | ---- | ------ | ---------------- |
| ｛YYYYMMDD｝ | num  | 掉粉数 | 字段名为日期     |
| ……           | num  | ……     | 近30天的掉粉情况 |

示例：

http://member.bilibili.com/x/web/index/stat

```json
{
	"code": 0,
	"message": "0",
	"ttl": 1,
	"data": {
		"fan_recent_thirty": {
			"follow": {
				"20200304": 0,
				"20200305": 1,
				"20200307": 1,
				"20200308": 0,
				"20200309": 1,
				"20200310": 6,
				"20200311": 0,
				"20200313": 0,
				"20200314": 0,
				"20200316": 3,
				"20200317": 0,
				"20200318": 1,
				"20200319": 2,
				"20200320": 0,
				"20200321": 0,
				"20200322": 2,
				"20200323": 5,
				"20200324": 4,
				"20200325": 2,
				"20200326": 2,
				"20200327": 3,
				"20200328": 1,
				"20200329": 1,
				"20200331": 1,
				"20200401": 2
			},
			"unfollow": {
				"20200304": 1,
				"20200305": 0,
				"20200307": 0,
				"20200308": 0,
				"20200309": 2,
				"20200310": 1,
				"20200311": 1,
				"20200313": 2,
				"20200314": 1,
				"20200316": 0,
				"20200317": 1,
				"20200318": 1,
				"20200319": 0,
				"20200320": 1,
				"20200321": 1,
				"20200322": 1,
				"20200323": 1,
				"20200324": 0,
				"20200325": 1,
				"20200326": 0,
				"20200327": 0,
				"20200328": 0,
				"20200329": 0,
				"20200331": 0,
				"20200401": 1
			}
		},
		"inc_coin": 0,
		"inc_elec": 0,
		"inc_fav": 0,
		"inc_like": 2,
		"inc_share": 0,
		"incr_click": 62,
		"incr_dm": 1,
		"incr_fans": 2,
		"incr_reply": 2,
		"total_click": 31059,
		"total_coin": 440,
		"total_dm": 522,
		"total_elec": 90,
		"total_fans": 390,
		"total_fav": 557,
		"total_like": 729,
		"total_reply": 405,
		"total_share": 254
	}
}
```



## UP主专栏状态数据

> http://member.bilibili.com/x/web/data/article

*方式：GET*

**json回复：**

| 字段    | 类型 | 内容     | 备注         |
| ------- | ---- | -------- | ------------ |
| code    | num  | 返回值   | 0：成功      |
| message | str  | 错误信息 | 默认为0      |
| ttl     | num  | 1        | 作用尚不明确 |
| data    | obj  | 信息本体 |              |

`data`对象：

| 字段       | 类型 | 内容       | 备注 |
| ---------- | ---- | ---------- | ---- |
| view       | num  | 总计阅读数 |      |
| reply      | num  | 总计评论数 |      |
| like       | num  | 总计点赞数 |      |
| coin       | num  | 总计投币数 |      |
| fav        | num  | 总计收藏数 |      |
| share      | num  | 总计分享数 |      |
| incr_view  | num  | 新增阅读数 |      |
| incr_reply | num  | 新增评论数 |      |
| incr_like  | num  | 新增点赞数 |      |
| incr_coin  | num  | 新增投币数 |      |
| incr_fav   | num  | 新增收藏数 |      |
| incr_share | num  | 新增分享数 |      |

示例：

http://member.bilibili.com/x/web/data/article

```json
{
	"code": 0,
	"message": "0",
	"ttl": 1,
	"data": {
		"view": 290,
		"reply": 17,
		"like": 34,
		"coin": 9,
		"fav": 15,
		"share": 7,
		"incr_view": 6,
		"incr_reply": 0,
		"incr_like": 0,
		"incr_coin": 0,
		"incr_fav": 0,
		"incr_share": 0
	}
}
```

