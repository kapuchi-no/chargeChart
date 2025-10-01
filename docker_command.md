# dockerコンテナセットアップ
## dockerのイメージ作成
docker build -t [tag_name:version] -f [Dockerfileの場所] .

## dockerのコンテナ作成
docker run --name [container_name] -it -d [tag_name:version]
- it：プロセスが終了しても起動したままにする
- d：バックグラウンド実行

# dockerの状況確認
##　dockerのイメージ一覧
docker images

## dockerのコンテナ一覧
### 動いているもの
docker ps

### 全部
docker ps -a

# dockerコンテナに対する操作
## dockerの中に入る
docker exec -it [container_name] sh

## コンテナを停止する
docker stop [container_name]

## コンテナを実行する
docker start [container_name]

## コンテナを削除する
docker rm [container_name]

# docker イメージに対する操作
## イメージを削除
docker rmi [image_name]

# docker compose
## dockerイメージ作成
docker compose build

## 単一サービスに対する操作
イメージ作成，コンテナ構築，コンテナ起動を行う
docker compose run [service_name] command

## すべてのサービスに対する操作
初回のみイメージの作成，コンテナの構築を行い，コンテナを起動する
docker compose up

## 作成済みのすべてのコンテナに対する操作
docker compose start