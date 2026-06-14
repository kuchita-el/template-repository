# template-repository

新規プロジェクト立ち上げ時に引き継ぐ、**言語非依存の共通基盤 (L1) 雛形**。

## 用途

「Use this template」で新規リポを作成し、言語/フレームワークに依存しない基盤ファイル一式を引き継ぐ。各プロジェクト固有（言語・CI・依存関係）の設定は作成後に追加する。

## 含まれるもの (L1)

| ファイル | 役割 |
|---|---|
| `.editorconfig` | エディタ基礎設定（charset / EOL / final newline / trailing whitespace / indent）。formatter と責務分離 |
| `.gitignore` | OS 生成物のみ（言語別 ignore は各プロジェクトで追加） |
| `CLAUDE.md` | プロジェクト規約の骨子（概要は空欄。user-scope 規約を参照） |
| `LICENSE` | MIT（年・著作権者は各プロジェクトで更新） |
| `.github/ISSUE_TEMPLATE/*`, `.github/PULL_REQUEST_TEMPLATE.md` | Issue / PR テンプレート |

## 含まれないもの（スコープ外）

- CI ワークフロー・devcontainer・`package.json` 等の言語/フレームワーク依存ファイル
- 言語別 `.gitignore`（Node / Python / Go 等は各プロジェクトで追加）
- フレームワーク特化雛形（`template-nextjs` 等は別リポとして将来検討）

## 使い方

1. GitHub で「Use this template」→ 新規リポ作成
2. `LICENSE` の年・著作権者を更新
3. `CLAUDE.md` のプロジェクト概要・技術スタック・コマンドを記入し、雛形メモ行を削除
4. 言語/フレームワーク固有の `.gitignore`・CI・依存関係を追加

## 補足

- リポジトリ設定（branch protection 等の Ruleset）は「Use this template」では複製されない仕様。これらは `github-config` リポ（Terraform / IaC）で別途管理する。
