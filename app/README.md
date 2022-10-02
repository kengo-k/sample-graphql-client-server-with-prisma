##### プロジェクトの作成
```
yarn init
yarn create next-app sample --ts
```

##### ライブラリのインストール

```
# ORM関連
yarn add -D prisma

# GraphQL関連
yarn add graphql
yarn add @apollo/client
yarn add -D @graphql-codegen/cli @graphql-codegen/typescript @graphql-codegen/typescript-resolvers
yarn add -D @graphql-codegen/typed-document-node @graphql-codegen/typescript-operations
```

##### DBの初期化

```
npx prisma init --datasource-provider sqlite
```

##### yamlファイルから型定義を生成する

- サーバ側の定義を生成

```
yarn run graphql-codegen --config graphql/codegen-server.yaml
```

- クライアント側の定義を生成

```
yarn run graphql-codegen --config graphql/codegen-client.yaml
```
