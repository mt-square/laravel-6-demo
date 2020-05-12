# Laravel
## local環境初回構築
- clone repo
- .env作成

```
cd src/
cp .env.example .env
```

- docker起動

```
docker-compose up --build -d
```

- docker 内に入る

```
docker exec -it laravel-demo-php bash
```

- composer

```
composer install
```

- DB定義

```
php artisan migrate
```

- テストデータ投入

```
php artisan db:seed
```

## local環境二度目以降の起動

```
docker-composer up -d
```

# git運用

## ブランチ
しばらくはdevelop一本運用で進め、ある程度形になって複数メンバでの開発が始まり次第、以下のブランチを用いた開発に移行する。

- master
  - 本番環境デプロイブランチ
- staging
  - 検証環境デプロイブランチ
- develop
  - 開発
- feature/
  - 機能
- fix/
  - 最初はなし
- hotfix/
  - 最初はなし
- refactor/
  - 最初はなし

## コミット prefix(参考)
- BREAKING CHANGE: 破壊的な変更 - メジャーアップデートが必要
- feat: 新しい機能の追加 - マイナーアップデートが必要
- fix: リリースノートに含めるような修正 - パッチアップデートが必要
- refactor: リファクタリング
- style: コードスタイル、スペースの調整など
- test: テストの追加、修正
- chore: その他
