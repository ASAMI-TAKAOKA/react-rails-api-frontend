## React と Rails API モードで簡単なアプリを作るサンプル
こちらの記事を参考にさせていただき、git cloneして使用させていただきました。
https://zenn.dev/tatsurom/articles/2b92156e509d9e27f81b

- バックエンド: https://github.com/ASAMI-TAKAOKA/react-rails-aop-backend
- フロントエンド: https://github.com/ASAMI-TAKAOKA/react-rails-aop-frontend

## 動かしてみる
フロント側  (3002番ポート)
1. `git clone git@github.com:tatsuro-m/react_rails_api_frontend.git`
2. プロジェクト直下に `.env` を作成し、 `REACT_APP_DEV_API_URL=http://localhost:3001` を記述。
3. package.jsonに "proxy": "http://localhost:3001", を記述。
4. `yarn && yarn start`
5. `localhost:3002` でReact アプリの起動確認
---
バックエンド側  (3001番ポート)
1. `git clone git@github.com:tatsuro-m/react_rails_api_backend.git`
2. `docker-compose up`
3. `docker-compose exec web /bin/ash`
4. コンテナ内で、 `rails db:create`, `rails db:migrate`, `rails db:seed`
---

これでReact アプリをリロードするとアプリが動くはず。 
