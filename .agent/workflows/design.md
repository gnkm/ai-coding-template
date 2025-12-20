---
description: 設計書を作る。
---

あなたは熟練したソフトウェアアーキテクトです。
以下の入力情報をもとに、実装フェーズに進むための **基本設計書 (`docs/design.md`)** を作成してください。

## 入力情報

1.  **要求仕様書**: `docs/requirements.md` (機能要件、非機能要件)
2.  **技術スタック**: `docs/tech_stack.md` (使用する言語、フレームワーク)

## 出力ドキュメント構成 (`docs/design.md`)

以下のセクションを含むマークダウンファイルを作成してください。

### 1. アーキテクチャ概要 (Architecture Overview)
*   システム全体の構成図 (Mermaid `graph TD` を使用)
*   Frontend (Tauri Webview) と Backend (Tauri Core) の責務分担
*   IPC (Inter-Process Communication) の設計方針

### 2. ディレクトリ構造 (Directory Structure)
*   プロジェクトの推奨ディレクトリ構成ツリー
*   主要なファイル/フォルダの配置意図

### 3. データフローと状態管理 (Data Flow & State Management)
*   ユーザー入力（キーイベント）から画面描画までのフロー
*   **モード管理 (Mode State)**: Vimモード/Emacsモードの状態遷移と保持方法
*   **PDFレンダリング**: PDFファイルのロードから表示、ページ移動の仕組み

### 4. コンポーネント設計 (Component Design)
*   主要なReactコンポーネントの定義 (例: `PDFViewer`, `StatusBar`, `CommandPalette`)
*   コンポーネント間の階層関係

### 5. IPC コマンド定義 (IPC Interface)
*   Frontend から Backend (Rust) を呼び出すためのコマンド一覧
    *   例: ファイルオープン、設定読み込み、メニュー制御など
    *   引数と返り値のデータ型

---

**注意事項:**
*   出力は **日本語** で行ってください。
*   コードの詳細は実装フェーズで決定するため、ここでは「どのモジュールが何をするか」という構造設計に集中してください。
*   Tauri v2 のベストプラクティス（セキュリティ、分離モデル）を意識した設計にしてください。
