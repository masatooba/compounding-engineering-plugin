---
name: plan_review
description: Have multiple specialized agents review a plan in parallel
argument-hint: "[plan file path or plan content]"
---

# すべての出力は日本語で行ってください

# /plan_review コマンド

プランを複数のエージェントで並列レビューします。

## 重要: レビューのみ、実装は行わない

**このコマンドはレビューのみを行います。実装は絶対に開始しないでください。**

- プランの問題点を指摘する
- 改善提案を行う
- リスクや懸念点を洗い出す
- **コードを書かない**
- **ファイルを編集しない**
- **実装を始めない**

## レビュー対象

<plan_to_review> $ARGUMENTS </plan_to_review>

## レビュー実行

以下のエージェントで並列レビューを実行：

- @agent-dhh-rails-reviewer - Rails設計の観点から
- @agent-kieran-rails-reviewer - コード品質の観点から
- @agent-code-simplicity-reviewer - シンプルさの観点から

## レビュー完了後

レビュー結果をまとめて報告し、**ユーザーの次の指示を待つ**。

以下のような選択肢を提示：
1. プランを修正する
2. このまま実装に進む（`/work`コマンドを使用）
3. 追加のレビューを行う
4. その他

**実装を勝手に開始してはいけません。必ずユーザーの明示的な指示を待ってください。**
