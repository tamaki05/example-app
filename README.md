## 開発環境構築
- .envファイルを設定する
- 以下のコマンドを実行する

```
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs

./vendor/bin/sail npm install
./vendor/bin/sail npm run dev
```