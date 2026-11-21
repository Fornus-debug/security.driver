# CLAUDE.md — Claude Code/AI作業ルール

## 共通開発コンテキスト（AI必読）
- 作業前にこのリポジトリの `AGENTS.md` / `CLAUDE.md` と `docs/project-context.md` / `docs/todo.md` / `docs/decisions.md` / `docs/handover.md` があれば確認し、未整備なら整備を提案する。
- 開発共通の再発防止ポリシー: https://github.com/Fornus-debug/github-context-collector/blob/main/docs/ai-development-policy.md
- そのポリシーが外部から読めない場合にも、最低限次を守る: 根本原因の確認、最小限の変更、秘密情報の非公開、本番相当の権限/DB/HTTP検証、0件とエラーの区別、外部APIの件数・時間・並列上限の設定。
- 最初に難易度/推奨モデル、現状、影響範囲、実施手順を説明。コマンドは1つずつ。破壊的削除・課金・公開・データ変更・外部送信は事前承認。無断の `rm` 禁止。
- 変更後は型/テスト/ビルドと必要な実動作を確認し、未検証は未検証と明記。docsの現状/タスク/判断/引継ぎの更新案と新しい失敗候補を残す。
- プロジェクト固有の厳しい安全規則・正本仕様は維持する。privateリポジトリの失敗詳細や秘密値をpublicへ移さない。
