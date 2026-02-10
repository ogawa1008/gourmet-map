# Gourmet Map

## 開発するもの・概要
地図上から飲食店を探せるグルメアプリを開発する。  
現在地周辺の飲食店を表示し、ジャンル・評価などで絞り込みができることを目標とする。
その他の機能として自分が気に入った店のセットを他人に共有できるものを作成する

チーム開発を前提とし、設計・実装・運用の流れをGitHub上で管理する。

---

## メンバー
- ogawa1008（リポジトリ管理・全体設計）
- 

---

## 使用技術（予定）
### フロントエンド
- （例）Reactなど

### バックエンド
- （例）Node.js / Firebase / Spring Boot など

### API
- 地図API（例：Google Maps API）
- 飲食店情報API（検討中）


## ファイル構成
```text
gourmet-map/
├─ frontend/        # フロントエンド
├─ backend/         # バックエンド
├─ docs/            # 設計ドキュメント
│  ├─ ui/           # 画面設計
│  └─ api/          # API設計
├─ assets/          # 画像・素材
├─ .gitignore
└─ README.md

開発ルール

ブランチルール
	•	main：完成版（直接コミット禁止）
	•	develop：開発用ブランチ
	•	feature/*：個人作業用ブランチ

作業ルール
	•	作業は必ず feature/* ブランチで行う
	•	develop に直接コミットしない
	•	作業完了後は Pull Request を作成する
	•	作業前は必ず最新の develop を取得する

⸻

使うコマンド一覧（これだけ覚えればOK）

### 初回セットアップ（最初だけ）
git clone https://github.com/ユーザー名/gourmet-map.git
cd gourmet-map

### 1作業を始めるとき（毎回）
git checkout develop
git pull
git checkout -b feature/作業名
例：git checkout -b feature/ui

### 2ファイルを編集したあと
git add .
git commit -m "作業内容を簡潔に書く"
例：git commit -m "UI画面のワイヤーフレームを追加"

### GitHubに送る
git push -u origin feature/ui

### 3他の人の変更を取り込みたいとき
git checkout develop
git pull
git checkout feature/ui
git merge develop

### 4作業が終わったら
	•	GitHubで Pull Request を作成
	•	feature/* → develop に向けてマージする

---

## 5Pull Request（PR）の出し方

### PRを出すタイミング
- 作業が一区切りついたとき
- 機能・設計が最低限動く状態になったとき

---

### PRの作成手順
1. 作業ブランチを push する
```bash
git push -u origin feature/作業名

---

## ⚠️ コンフリクト時の対処手順（README追記用）

```md
---

## ⚠️ コンフリクト（衝突）が起きたとき

### コンフリクトとは
同じファイルの同じ行を  
複数人が同時に変更したときに起こる衝突のこと。

---

### コンフリクトが起きるタイミング
- `git merge develop` をしたとき
- Pull Request をマージするとき

---

### 対処手順（基本）
1. まず落ち着く（壊れていない）
2. どのファイルで起きているか確認
```bash
git status

注意
	•	勝手にブランチを消さない
	•	コンフリクトが出たら無理に直さず共有する
	•	分からないことは README を先に読む
