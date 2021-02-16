# docker-flask-mysql

### 概要
Dockerを使ってFlaskとMySQLで簡易的なWeb API環境を構築

### 構築手順
```
cd {クローンしたフォルダ}
docker-compose build
docker-compose up -d
```

### API仕様
#### データ登録
以下の形式で、ユーザID、ユーザ名、ユーザの住所の情報を登録できる。
ASCIIのみ対応。
```
curl -X POST http://localhost:8000/user?id={ユーザID}\&username={ユーザ名}\&address={ユーザの住所}
```

#### データ検索
以下の形式で、ユーザ名をキーに、ヒットしたユーザ全員をJSON形式で取得できる。
ユーザ名は曖昧検索で検索される。
curl -X GET http://localhost:8000/user?username={検索語}
