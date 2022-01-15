# frourio sample
> frourioの検証

## Steps of what has been done
- `create-frourio-app`での環境構築
- `docker-compose.yml`にpostgresのサービスを追加
- `client`ディレクトリにNuxtのソースを移行
- `tsconfig.json`のpath aliasの設定を変更
  - `@/`で`./client`を向くように

## Notes
- 最初にDBのプロセスが立ってないとInitializeに失敗するので、Dockerなどで用意しておく必要がある
  - 今回は`Skip DB connection checks`を`No`にして、Initializeが終わってから`docker-compose.yml`を作成しDBのサービスを追加・起動して`yarn dev`を実行すると無事マイグレーションが走った
