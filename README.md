# laravel-setup-base

## Docker 用 .env作成(プロジェクト直下)
touch .env

## .envに以下を記述（UID/GIDはホストOSのユーザーIDに合わせて設定）
Linux 環境の一般ユーザーは多くの場合、以下の値になります UID=1000 GID=1000
UID=1000
GID=1000

他の環境では以下のコマンドでホストユーザーのUID/GIDを確認し、同じ値を記述してください
id

### Docker ビルド 
docker-compose up -d --build

### PHPコンテナに入る 
docker-compose exec php bash

### Composer インストール 
composer install

### .env 作成 
cp .env.example .env

### アプリキー生成 
php artisan key:generate

PHPコンテナから出る　Ctrl+D

