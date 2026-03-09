# trpg-session タスク管理

## 現在の状態（2026-03-04）

Phase 1 完了。Phase 2 の作業待ち。

### Phase 1 完了済み

- [x] Next.js 15 + TypeScript + Tailwind + shadcn/ui セットアップ
- [x] Supabase型定義 (`src/lib/database.types.ts`)
- [x] BCDice APIクライアント (`src/lib/bcdice.ts`) — フォールバック汎用パーサー付き
- [x] ランディングページ（ルーム作成/入室）
- [x] セッションページ `/room/[roomId]`
- [x] チャット + Supabase Realtime リアルタイム同期
- [x] ダイス表示（成功/失敗/クリティカル/ファンブル色分け）
- [x] ユーザー一覧（Supabase Presence）
- [x] ゲームシステム選択（BCDice全システム）
- [x] `.env.local` にSupabase URLとanon keyを設定
- [x] 動作確認（ルーム作成 → チャット → ダイスロール）

### バグ修正メモ

- BCDice `/v2/game_system` API は `sort_key`（snake_case）で返すが、コードは `sortKey`（camelCase）を期待していた → `fetchGameSystems()` 内でマッピングして修正済み

## Phase 2 候補（優先度順）

1. キャンバス + トークン（Konva.jsで2Dマップ）
2. BGM/SEプレイヤー
3. キャラクターシート（システム非依存KV表）
4. ハンドアウト（GM→特定PL秘匿配信）
5. ユーザー認証 + GM/PL権限分離
