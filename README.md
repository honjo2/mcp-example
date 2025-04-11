# mcp-example

MCPサーバーのサンプルコードです。

## MCPサーバ作成手順

```sh
mkdir mcp-example
cd mcp-example
npm init -y
npm install @modelcontextprotocol/sdk zod
npm install -D @types/node typescript
mkdir src
touch src/index.ts
vi package.json
vi tsconfig.json
vi index.ts
npm run build
```

## MCPクライアント（Claudeデスクトップアプリ）に追加

claude_desttop_config.jsonに以下追加しClaudeデスクトップアプリを再起動
```json
"mcp-example": {
  "command": "/Users/honjo2/.local/share/mise/shims/node",
  "args": [
    "/Users/honjo2/workspace/test/mcp-example/build/index.js"
  ]
}
```

## MCPクライアント（Roo Code）に追加

Roo Codeの上部のMCP ServersのグローバルMCPを編集で開くjsonファイルに上記同様のものを追加

## 使い方

Claudeデスクトップアプリで「double_numberを使って3を2倍した結果を表示して」と入力する

## 参考

- [簡易な自作MCPサーバーをお試しで実装する方法](https://zenn.dev/smartround_dev/articles/02af1058e9f80f)
