# Git/GitHub 速習コツメモ

> 迷ったらこの1枚だけ見ればOK。VS Code 前提。

## 毎回の最小ルーチン（3手）
1) 変更する（書く・画像貼る）  
2) **Commit**（メッセージ → ✓）  
3) **Push**（`Ctrl+Shift+P` → *Git: Push*）

## 迷子にならない設定（1分）
- `git.enableSmartCommit`: **true**（未ステージでも✓でコミット）  
- `git.autofetch`: **true**（リモート更新を自動取得）  
- `git.showSyncButton`: **true**（必要なら“Sync”を表示）

> 設定は `Ctrl+,` で開けます。

## すぐ確認するコマンド（覚えるのはこれだけ）
```bash
git status -sb        # 今の状態（push/pull必要か）
git push              # 送る（手元 → GitHub）
git pull --rebase     # 受け取る（GitHub → 手元、衝突少なめ）
```

## つまずいたら
- Push が拒否 → 先に `git pull --rebase` → 競合が出たらVS Codeで解決 → `git push`
- Publish/Sync が見えない → `Ctrl+Shift+P` → 「Git: Push」
- リモート未設定 → `git remote -v` が空 → `git remote add origin <URL>` → `git push -u origin main`

## 習慣化のコツ
- **章を書き終えたら必ず Commit → Push** をセットにする  
- 1日1回、GitHub のリポで**更新時刻が動いているか**だけ確認
