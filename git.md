# GITの使い方  

### 新しく使うディレクトリ
``` 
git init    //ディレクトリを指定する
git add README.md   //ファイルを指定する
git commit -m "first commit"    //ローカルリポジトリに移す
git branch -M main  //ブランチの設定
git remote add origin git@github.com:riku0202/a.git /リモートレポジトリを指定
git push -u origin main //  コミットしたファイルをプッシュする
```
### 既存のディレクトリ
```
git remote add origin git@github.com:riku0202/a.git     
git branch -M main
git push -u origin main
```
https://docs.github.com/ja/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent 
1. 新しいSSHキーを生成してssh-agentに追加する
2. Githubアカウントへの新しいSSHキーの追加   

