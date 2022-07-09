### 初回起動時
- poetry を使ってFastAPIをインストールし、 pyproject.toml を作成

```
docker-compose run \
  --entrypoint "poetry init \
    --name demo-app \
    --dependency fastapi \
    --dependency uvicorn[standard]" \
  demo-app

```

- FastAPIのインストール
`docker-compose run --entrypoint "poetry install" demo-app`

- pytest install (develop環境のみ)
`docker-compose exec demo-app poetry add -D pytest-asyncio aiosqlite httpx`

### docker 立ち上げ
`docker-compose build --no-cache`

### 各種実行コマンド
testの実行
`docker-compose run --entrypoint "poetry run pytest" demo-app`

参考: https://zenn.dev/sh0nk/books/537bb028709ab9/viewer/d3f074
