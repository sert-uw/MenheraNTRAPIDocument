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

## GET http://hostname:port/girls/:girl_id/response_candidates?token=abcd1234efg

### Response 200

```
[
  { "id": 1, "short_text": "何?", "text": "どうしたの?" },
  { "id": 2, "short_text": "好き", "text": "好きだよ" },
]
```

### Response 422

認証エラー

# メッセージ取得

## GET http://hostname:port/girls/:girl_id/messages?token=abcd1234efg

### Response 200

```
[
  { "id": 1, "message_list_id": 1, "text": "寂しい" },
  { "id": 2, "message_list_id": 3, "text": "なんでもない" },
]
```

### Response 422

認証エラー

# メッセージ既読

## PUT http://hostname:port/girls/:girl_id/messages/:id

### Request

どのメッセージまで既読にするか(:idで指定)

```
{
  "token": "abcd1234efg"
}
```

### Response 200

### Response 422

認証エラー

# メッセージへ返信

## POST http://hostname:port/girls/:girl_id/messages

### Request

`candidate_id`: 返信に選んだ候補テキストID

```
{
  "token": "abcd1234efg",
  "candidate_id": 1
}
```

### Response 200

### Response 422

認証エラー
