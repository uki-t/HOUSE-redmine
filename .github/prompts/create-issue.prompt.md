---
description: Redmineに新しいチケットを作成する
---

新しいRedmineチケットを作成します。

まず以下の情報を確認してください（不明な場合は一覧APIで取得）：
- プロジェクト一覧: `GET /projects.json`
- チケット種別: `GET /trackers.json`
- 優先度一覧: `GET /enumerations/issue_priorities.json`

次に作成に必要な情報を聞いてから、`POST /issues.json` でチケットを作成してください。

必須項目：
- `project_id`: プロジェクトID
- `subject`: チケットのタイトル

任意項目：
- `tracker_id`: チケット種別
- `priority_id`: 優先度
- `description`: 詳細説明
- `assigned_to_id`: 担当者ID
- `due_date`: 期日 (YYYY-MM-DD)
- `estimated_hours`: 予定工数

作成後は作成されたチケットのIDとURLを表示してください。
