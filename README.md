📘 README.md（プロジェクト環境構築まとめ）
# Illust_Share - Development Setup

このプロジェクトで行った環境構築の手順をまとめています。  
Windows 環境 + Laravel + GitHub を利用した構成です。

---

## 📌 1. 開発環境の準備

### ✔ PHP / Apache / MySQL（XAMPP）
Windows で PHP を簡単に使うために **XAMPP** をインストール。

インストール後、以下で動作確認：

```bash
php -v

📌 2. Composer のインストール

Laravel を使うために必要なので公式インストーラーから導入。

👉 https://getcomposer.org/Composer-Setup.exe

インストール中に XAMPP の php.exe を指定：

C:\xampp\php\php.exe


動作確認：

composer -V

📌 3. Laravel プロジェクトの作成

空のフォルダを作り、そこで以下を実行：

composer create-project laravel/laravel .


Do you want to remove the existing VCS (.git...) history?
→ y を入力して削除。

📌 4. Git の初期設定（ユーザー情報）
git config --global user.name "あなたの名前"
git config --global user.email "あなたのメールアドレス"

📌 5. Git リポジトリの初期化

Laravel プロジェクトフォルダ内で実行：

git init
git add .
git commit -m "Initial Laravel project"

📌 6. GitHub との接続 (remote 設定)
git remote add origin https://github.com/あなた/Illust_Share.git
git branch -M main


GitHub 側が空でない場合は削除して空にしておく。

📌 7. GitHub へ初回 push（強制）
git push -u origin main --force


成功すると、GitHub リポジトリに Laravel の構成が反映される。

📌 8. Laravel の動作確認

ローカルで Laravel を起動：

php artisan serve


ブラウザから以下にアクセス：

http://127.0.0.1:8000


Laravel の初期画面が表示されれば環境構築完了。