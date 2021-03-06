# 環境構築
- yarnを使う
- nodeのバージョンは v14.15.1
- nodenvを使うと便利

1. ローカルにクローンする
```git
git clone "URL"
```
2. node_modulesをインストールする
```yarn
yarn install
```
3. 起動
```yarn
yarn dev
```

# json-server起動

1. 起動
```yarn
yarn api-json
```
2. エンドポイントにアクセス

> http://localhost:3001/posts　　
> http://localhost:3001/comments　　
> http://localhost:3001/profile

3. フロント側で各エンドポイントのAPIを叩くと、src/db/db.jsonに記述したjsonデータを受け取ることができる

# graphql-json-server起動

1. 起動
```yarn
yarn api
```
2. エンドポイントにアクセス

> http://localhost:4000

3. フロント側でエンドポイントにアクセスしてクエリーを投げると、src/database/graphql_db.jsに記述したjsonデータを受け取ることができる

4. http://localhost:4000でエミュレーターを起動して次のクエリーを投げてみる
```gql
{
  appPosts{
    id
    title
    view
  }
}
```



# git コミットルール
1. コミットメッセージの先頭にはGitmojiとプレフィックスをつける  
2. 絵文字の後は半角スペース
3. :以降は日本語使って説明
4. 具体的な変数や関数を入れる

> ✨ event:データベースに保存するhandleSave()を作成

- 🔥
  - cmt:コメント削除 
  - file:fileごと削除した時
  - log:不要なconsole.log等を削除した時
  - lib:package.jsonのパッケージを削除した時
  - config:configのruleとか削除した時
- ✨
  - ui:コンポーネント作成・更新
  - page:新規ページ作成・更新
  - event:イベント関数作成・更新
  - db:json-server作成・更新
- ♻️ 
  - cmt:詳解コメント追加した時など
  - ui:コンポーネント共通化した時など
  - event:イベント関数を共通化した時など
  - style:cssを変数化して共通化した時など
- 🚚
  - move:ファイル移動
- 🔧
  - add:configファイルのruleとか追加した時
- ➕
  - add:ライブラリ追加
  - update:バージョン更新
- 🐛
  - fix:重度のバグ
- 🩹
  - fix:軽度のバグ
- 📝
  - update:README更新時
- ✅
  - test:テストコード&サンプルコード

