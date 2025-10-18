# Git & GitHub 概要メモ（最短で運用するための覚え書き）

## 0. これは何？
- **Git**：ファイルの変更履歴をローカルで管理するツール（履歴＝コミット）。
- **GitHub**：その履歴をインターネット上で共有・バックアップする場所（リモート）。
- VS Code から **Commit → Push → Pull** の3手を覚えれば日常運用はOK。

---

## 1. よく出る用語（超要点）
- **Repository（リポジトリ）**：プロジェクトの入れ物。フォルダ＋履歴。
- **.git/**：フォルダを Git 化する“心臓”。これがあると Git 管理下。
- **Stage（ステージ）**：コミットに含める変更を選ぶこと。
- **Commit（コミット）**：変更をひとかたまりの**履歴**として保存（ローカル）。
- **Push**：ローカルの履歴を **GitHub へ送る**。
- **Pull**：GitHub の履歴を **ローカルへ取り込む**。
- **Branch（ブランチ）**：作業の枝。デフォルトは `main`（または `master`）。

> 覚え方：**Commit＝写真で保存、Push＝雲へアップ、Pull＝雲から取り込み**。

---

## 2. 日常の最小ワークフロー（3手）
1. 変更する（記事を書く・画像を追加）  
2. **Commit**（節目の保存）  
3. **Push**（GitHub へ）

### VS Code 操作
- メッセージ入力 → **✓ Commit** → `Ctrl+Shift+P` → **Git: Push**
- 取り込みたい時は `Ctrl+Shift+P` → **Git: Pull (Rebase)**

### コマンド派
```bash
git add .
git commit -m "update: 記事/画像"
git push
```

---

## 3. 新規セットアップ（ローカル → GitHub）
1. ローカルで初期化＆初回コミット
   ```bash
   git init
   git add .
   git commit -m "first commit"
   git branch -M main
   ```
2. GitHub で空のリポを作成（README なし）、URL を取得  
3. リモート登録 → プッシュ
   ```bash
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```

---

## 4. 状態確認の定番
```bash
git status              # 変更の有無
git remote -v           # リモートのひもづけ
git log --oneline -5    # 直近5コミット
git status -sb && git fetch && git status -sb
# ↑ push/pull が必要か（ahead/behind）を一目で
```

---

## 5. つまずき→対処（覚えるのはこれだけ）
- **Push が拒否された（non-fast-forward）**  
  → 先に取り込む：`git pull --rebase` → 競合が出たら VS Code で解決 → `git push`
- **remote origin already exists**  
  → URL 入れ直し：`git remote set-url origin <URL>`
- **ブランチ名違い（master）**  
  → コマンド内の `main` を `master` に読み替え
- **今どこまでできてる？を確認したい**  
  ```bash
  git rev-parse --is-inside-work-tree  # trueならGit管理中
  git branch                           # 現在ブランチに * が付く
  git remote -v                        # ひも付き確認
  ```

---

## 6. ファイル共有のコツ（今回の執筆環境）
- `.vscode/settings.json`：**コミットOK**（書く環境の統一に効く）
- `style.css`（プレビュー用カスタムCSS）：プロジェクト直下に置き、各 `.md` 冒頭に
  ```html
  <link rel="stylesheet" href="./style.css">
  ```

---

## 7. もう少し慣れたら
- コミットを小さく意味のある単位に（後で戻しやすい）
- `git commit --amend`（直前のメッセージ修正）
- `git revert <コミットID>`（安全に取り消す）

---

### 最後に：迷ったらこの順番
1) `git status` を見る  
2) **Commit** できる内容ならコミット  
3) 送るなら **Push**、受け取りたいなら **Pull**
