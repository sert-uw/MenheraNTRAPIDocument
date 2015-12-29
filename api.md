# ユーザ登録

## POST http://hostname:port/users

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

## GET http://hostname:port/girls

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

# 返信候補取得

## GET http://hostname:port/girls/:id/response_candidates

### Response

```
[
  { "id": 1, "candidate": "どうしたの?" },
  { "id": 2, "candidate": "好き" },
]
```

# メッセージ取得

## GET http://hostname:port/girls/:id/messages

### Response

```
[
  { "id": 1, "body": "寂しい" },
  { "id": 2, "body": "なんでもない" },
]
```

# メッセージ既読

## PUT http://hostname:port/girls/:id/messages

### Request

どのメッセージまで既読にするか

```
{ "id": 30 }
```

### Response 200

# メッセージへ返信

## POST http://hostname:port/girls/:id/responses

### Request

```
{
  "response_id": 1
}
```

### Response 200
