# ユーザ登録

## POST http://hostname:port/users

### Request

```
{
  "name": "user_name",
  "uuid": "usid-dfsa-dfst",
  "device_type": "android or ios",
  "device_token": "dfdsgokjsadf"
}
```

### Response

```
{
  "token": "abcd1234efg"
}
```

# 女の子一覧取得

## GET http://hostname:port/girls?token=abcd1234efg

### Response 200

```
[
  {
    "id": "1",
    "name": "naoka",
    "is_couple": boolean,
    "spirit": 30,
    "dependence": 60
  },
]
```

### Response 422

認証エラー

# 返信候補取得

## GET http://hostname:port/girls/:id/response_candidates?token=abcd1234efg

### Response 200

```
[
  { "id": 1, "text": "どうしたの?" },
  { "id": 2, "text": "好き" },
]
```

### Response 422

認証エラー

# メッセージ取得

## GET http://hostname:port/girls/:id/messages?token=abcd1234efg

### Response 200

```
[
  { "id": 1, "body": "寂しい" },
  { "id": 2, "body": "なんでもない" },
]
```

### Response 422

認証エラー

# メッセージ既読

## PUT http://hostname:port/girls/:id/messages

### Request

どのメッセージまで既読にするか

```
{
  "token": "abcd1234efg",
  "id": 30
}
```

### Response 200

### Response 422

認証エラー

# メッセージへ返信

## POST http://hostname:port/girls/:id/responses

### Request

```
{
  "token": "abcd1234efg",
  "response_id": 1
}
```

### Response 200

### Response 422

認証エラー
