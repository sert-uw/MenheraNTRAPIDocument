# ユーザ登録

## POST http://sert.luna.ddns.vc:3000/users

### Request

```
{
  "name": "user_name"
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
    "name": "naoko",
    "is_couple": boolean,
    "spirit": 30,
    "dependent": 60
  },
]
```
