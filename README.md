# これは何

Laravel練習用のリポジトリ。
Laravel Breezeを使って簡易に構築した。

# 起動方法

Laravel Sailを利用しているため、Dockerが利用できることが前提。

```bash
./vendor/bin/sail up -d
```

# 動作確認方法

Postmanを利用する。

各種エンドポイントへのリクエストには、Sanctumにより発行される `XSRF-TOKEN` が必要で、[こちら](https://qiita.com/b95oss/items/8478c99583d72812d313)に設定方法が記載されている。

設定後、以下にリクエストしてユーザー情報が返却されていればOK

- POST /register
  - 以下をBodyに設定する
    - email
    - name
    - password
    - password_confirmation
- GET /api/user
