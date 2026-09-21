# karaage-soft-apps

からあげソフトのアプリの、公開しておく必要があるページを置くところ。
GitHub Pages で配信する。**アプリのソースはここには置かない。**

置いてあるのは、ストアの掲載欄から参照されるページだけ。
プライバシーポリシーのように「ログイン不要で誰でも読めるURL」が
求められるものが対象。

## 中身

| 場所 | 何 | URL |
| --- | --- | --- |
| `index.html` | 入口。アプリの一覧 | https://karaagesoft.github.io/karaage-soft-apps/ |
| `sudoku/privacy-policy.html` | 数独のお勉強 プライバシーポリシー | https://karaagesoft.github.io/karaage-soft-apps/sudoku/privacy-policy.html |

アプリが増えたら、`<アプリ名>/` を足していく。

## 直すとき

**このリポジトリのファイルは写し。** 元はアプリ側のリポジトリにある。

| ここ | 元 |
| --- | --- |
| `sudoku/privacy-policy.html` | `sudoku-app` の `publish/privacy-policy.html`（本文は `docs/privacy-policy.md`） |

元を直してから、ここへ写してコミットする。ここだけ直すと、次に写したときに
元へ戻ってしまう。

```powershell
Copy-Item ..\sudoku-app\publish\privacy-policy.html .\sudoku\privacy-policy.html
git add -A; git commit; git push
```

## GitHub Pages の設定

リポジトリの Settings → Pages で、Source を「Deploy from a branch」、
ブランチを `main`、フォルダを `/ (root)` にする。数分で上のURLが開く。
