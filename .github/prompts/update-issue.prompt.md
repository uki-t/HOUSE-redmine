---
description: Redmineのチケットのステータスや内容を更新する
---

Redmineチケットを更新します。

更新対象のチケットIDと変更したい内容を確認してから、`PUT /issues/:id.json` で更新してください。

よく使う更新内容：
- ステータス変更: `{"issue": {"status_id": <id>}}`
  - ステータス一覧: `GET /issue_statuses.json`
- 担当者変更: `{"issue": {"assigned_to_id": <id>}}`
- 進捗率更新: `{"issue": {"done_ratio": 50}}`
- コメント追加: `{"issue": {"notes": "コメント内容"}}`
- 期日変更: `{"issue": {"due_date": "2026-04-01"}}`

更新後は変更内容を確認して結果を報告してください。
