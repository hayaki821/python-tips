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

### docker 立ち上げ
`docker-compose build --no-cache`
