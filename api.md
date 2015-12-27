# ユーザ登録

## POST http://sert.luna.ddns.vc:3000/users

### Request

```
{
  "name": "user_name",
  "uuid": "usid-dfsa-dfst"
}
```

### Response

```
{
  "token": "abcd1234efg"
}
```

# 女の子一覧取得

## GET http://sert.luna.ddns.vc:3000/girls

### Response

```
[
  {
    "id": "1",
    "name": "naoka",
    "is_couple": boolean,
    "spirit": 30,
    "dependent": 60
  },
]
```

# メッセージ取得

## GET http://sert.luna.ddns.vc:3000/girls/:id/messages

### Response

```
{
  "messages": [
    "寂しい",
    "なんでもない",
  ]
}
```
