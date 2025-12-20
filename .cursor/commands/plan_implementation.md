---
description: 実装計画を立案する。
---

あなたはテクニカルプロジェクトマネージャー（TPM）です。
以下の入力情報をもとに、実装手順を詳細に定義した **実装計画書 (`docs/implementation_plan.md`)** を作成してください。

## 入力情報

1.  **要求仕様書**: `docs/requirements.md`
2.  **技術スタック**: `docs/tech_stack.md`
3.  **基本設計書**: `docs/design.md` (存在しなければ、この段階で簡易的にアーキテクチャを想定する)
4.  **開発ルール**: `AGENTS.md` (特に **TDD** と **Commit Granularity** について)

## 作成方針

本プロジェクトは **Test-Driven Development (TDD)** を厳格に適用します。
一度に大量のコードを書くのではなく、**「テスト作成 → 実装 → リファクタリング」** の小さなサイクルを回せるような粒度でタスクを分解してください。

## 出力ドキュメント構成 (`docs/implementation_plan.md`)

以下のフェーズに分けて、チェックリスト形式で記述してください。

### Phase 1: プロジェクト初期化 (Setup)
*   Tauri プロジェクトのスカッフォールディング作成 (`pnpm create tauri-app`)
*   Linter/Formatter の設定
*   CI/CD (GitHub Actions) の初期設定

### Phase 2: コア機能実装 (Core / Backend)
*   **TDDアプローチ**: Rust側のコマンド実装（ファイル読み込み等）に対するユニットテストと実装。

### Phase 3: フロントエンド基盤 (Frontend Foundation)
*   React コンポーネントのセットアップ
*   PDF表示ライブラリ (`react-pdf`) の導入と表示確認
*   キーイベントハンドラの実装（Vim/Emacs モード状態管理）

### Phase 4: 機能実装 (Features)
*   ページ移動ロジックの実装（TDD）
*   検索機能の実装（TDD）
*   ズーム機能等の補助機能

### Phase 5: 仕上げ (Polish)
*   UI/UX の調整（CSS）
*   アイコン設定、ビルド設定
*   全体を通した動作確認

---

**注意事項:**
*   出力は **日本語** で行ってください。
*   各タスク項目には、編集対象となるファイル名や、実行すべきコマンドを具体的に記述してください。
*   特に「テストを先に書く」という手順を明示的にタスクに含めてください。
