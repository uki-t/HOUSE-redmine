# Redmine プロジェクト コンテキスト

このリポジトリはローカルで動作する Redmine 環境の設定です。

## 環境情報

- **Redmine URL**: http://localhost:8080
- **MySQL**: localhost:13306
- **起動コマンド**: `docker compose up -d`

## Redmine REST API

認証情報は `.env` ファイルに記載されています。

### API キー認証（推奨）

```bash
source .env
curl -H "X-Redmine-API-Key: $REDMINE_API_KEY" http://localhost:8080/issues.json
```

### Basic 認証

```bash
curl -u admin:adminadmin http://localhost:8080/issues.json
```

## 主要エンドポイント

| 操作 | メソッド | エンドポイント |
|------|----------|----------------|
| チケット一覧 | GET | `/issues.json` |
| チケット詳細 | GET | `/issues/:id.json` |
| チケット作成 | POST | `/issues.json` |
| チケット更新 | PUT | `/issues/:id.json` |
| チケット削除 | DELETE | `/issues/:id.json` |
| プロジェクト一覧 | GET | `/projects.json` |
| プロジェクト詳細 | GET | `/projects/:id.json` |
| ユーザー一覧 | GET | `/users.json` |
| バージョン一覧 | GET | `/projects/:id/versions.json` |
| チケット種別 | GET | `/trackers.json` |
| ステータス一覧 | GET | `/issue_statuses.json` |
| 優先度一覧 | GET | `/enumerations/issue_priorities.json` |
