# localメール送信テスト

1. コンテナ起動
```sh
docker compose up -d
```

2. メール送信
```sh
docker compose exec postfix-sender bash
mail.txtの中身を貼り付け
```

3. メールが送信されていることを確認
```sh
docker compose exec postfix-recipient bash
cat /root/MailDir/new/送信されたファイル
```