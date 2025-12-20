# AI Coding Template

AI Agent との協働開発（Pair Programming with AI）を前提に設計された、高品質なプロジェクトテンプレートです。
セキュリティ、品質管理、そして AI とのコラボレーションを円滑にするためのワークフローがあらかじめ組み込まれています。

## 特徴 (Features)

*   **🛡️ セキュリティ & 品質管理**:
    *   [Lefthook](https://github.com/evilmartians/lefthook) による Git Hooks 管理。
    *   [Gitleaks](https://github.com/gitleaks/gitleaks) によるシークレットスキャン。
    *   [OSV-Scanner](https://github.com/google/osv-scanner) による脆弱性スキャン。
*   **🤖 AI Agent Workflows**:
    *   AI コーディングアシスタント（Antigravity, Cursor）向けに最適化されたワークフロー定義 (`.agent/workflows/`)。
    *   定型タスク（コミット、リファクタリング、設計、実装計画など）をスラッシュコマンドで実行可能。
*   **📝 ドキュメント標準**:
    *   開発の指針となる [CONTRIBUTING.md](./CONTRIBUTING.md) を完備。
    *   ISO/IEC/IEEE 29148:2018 に準拠した要求仕様策定フローをサポート。

## 始め方 (Getting Started)

### 前提条件 (Prerequisites)

*   Git
*   [Lefthook](https://github.com/evilmartians/lefthook)
*   [Gitleaks](https://github.com/gitleaks/gitleaks)
*   [OSV-Scanner](https://github.com/google/osv-scanner)

### セットアップ (Setup)

このテンプレートを使用してリポジトリを作成したら、以下のコマンドで Git Hooks を初期化してください。

```bash
# Install specific tools (macOS example)
brew install lefthook gitleaks osv-scanner

# Initialize Lefthook
lefthook install
```

## 使い方 (Usage)

### AI Agent との協働

このリポジトリには、AI Agent に指示を出すための「ワークフロー」が定義されています。
対応する AI エディタやエージェントを使用している場合、以下のコマンドでタスクを効率化できます。

| コマンド | 説明 |
| :--- | :--- |
| `/design` | 基本設計書の作成・更新 |
| `/plan_implementation` | 実装計画の立案 |
| `/start` | タスクの実装開始（TDDサイクル等） |
| `/commit` | コミットメッセージの生成とコミット |
| `/refactor` | コードのリファクタリング |

詳細は [CONTRIBUTING.md](./CONTRIBUTING.md) を参照してください。

## ライセンス (License)

[MIT License](./LICENSE)
