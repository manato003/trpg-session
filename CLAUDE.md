# CLAUDE.md — trpg-session

共通ワークフロー・原則は `C:/Dev/claude/CLAUDE.md` に定義されており自動適用される。

---

## プロジェクト固有のルール

- Supabase Realtimeの購読は `SessionRoom.tsx` 一箇所に集約する（分散させない）
- BCDice APIコールは `lib/bcdice.ts` 経由のみ（直接fetchしない）
- UIはTailwind CSS v4 + shadcn/ui。カスタムCSSを追加する前にshadcnコンポーネントで代替できるか確認
- `git add .` は禁止（`.nul` ファイル混入リスク）。ファイルを個別に指定する

---

## セッション開始時のチェックリスト

- [ ] `session-start` スキルをトリガー
- [ ] `docs/project_context.md` を読む

---

## タスク管理

| ファイル | 用途 |
|---|---|
| `tasks/todo.md` | 実装チェックリスト |
| `tasks/lessons.md` | PJ固有の教訓 |
