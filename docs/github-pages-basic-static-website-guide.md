---
marp: true
theme: default
paginate: true
---

# GitHub Pagesを使用した静的ウェブサイト公開手順

前提条件：GitHubアカウントは既に作成済み

---

## GitHub Pagesとは

- GitHubが提供する静的サイトホスティングサービス
- GitHubリポジトリから直接ウェブサイトを公開可能
- HTMLやCSS、JavaScriptファイルをホスティング
- 個人、組織、プロジェクトの簡単なウェブサイトに最適
- 無料で利用可能（パブリックリポジトリの場合）

---

## GitHub Pagesの主な特徴と制限

1. 簡単な設定：リポジトリの設定から数クリックで有効化
2. 自動デプロイ：mainブランチへのプッシュで自動更新
3. バージョン管理：Gitの機能を活用してサイトの変更履歴を管理
4. コラボレーション：チームでのウェブサイト開発が容易
5. 制限：
   - 静的コンテンツのみをホスティング可能
   - WordPressのような動的サイトは作成できない
   - サーバーサイドの処理やデータベース操作は不可能

---

## 1. 新しいリポジトリの作成

- GitHubにログイン後、ダッシュボードで「New」ボタンをクリック
- リポジトリ名を「my-first-site」に設定
- 「Public」を選択
- 「Add a README file」にチェック
- 「Create repository」をクリック

---

## 2. ローカル環境へのクローン

```bash
git clone https://github.com/あなたのユーザー名/my-first-site.git
cd my-first-site
```

---

## 3. ウェブサイトコンテンツの作成

- `index.html`ファイルを作成し、基本的なHTML構造を記述

例：

```html
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Site</title>
</head>
<body>
    <h1>Welcome to My First Site!</h1>
    <p>This is a simple website hosted on GitHub Pages.</p>
</body>
</html>
```

---

## 4. 変更をコミットしてプッシュ

```bash
git add .
git commit -m "初期ウェブサイトコンテンツを追加"
git push origin main
```

---

## 5. GitHub Pagesの有効化

- リポジトリのSettingsタブをクリック
- 左サイドバーの「Pages」を選択
- 「Source」セクションで「Deploy from a branch」を選択
- 「Branch」ドロップダウンで「main」を選択し、フォルダを「/ (root)」に設定
- 「Save」をクリック

---

## 6. サイトの公開確認

- 設定後、数分待つ
- 「Your site is live at <https://あなたのユーザー名.github.io/my-first-site/」というメッセージが表示される>
- 表示されたURLにアクセスして、サイトが正しく公開されているか確認

---

## 7. 更新とメンテナンス

- ローカルで`index.html`を編集し、新しいコンテンツを追加
- 変更をコミットしてプッシュ：

  ```bash
  git add .
  git commit -m "コンテンツを更新"
  git push origin main
  ```

- 数分後、GitHub Pagesに反映される

---

# 完了

おめでとうございます！これでGitHub Pagesを使用した基本的な静的ウェブサイトの公開が完了しました。
引き続き、HTMLファイルの編集を通じてコンテンツを更新し、ウェブサイトを発展させていってください。
