# GITの使い方  

### 新しく使うディレクトリ
``` 
git init    //.gitファイルが生成され、このファイルより下位にあるフォルダがgit管理される
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
[GithubDocs](https://docs.github.com/ja/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent )
1. 新しいSSHキーを生成してssh-agentに追加する
2. Githubアカウントへの新しいSSHキーの追加

### 新しいSSHキーを生成してssh-agentに追加する
  ```
  ssh-keygen -t ed25519 -C "riku0202excalibur@gmail.com"   //メールアドレスをラベルとしてSSHキーを作成
  cd.ssh
  eval "$(ssh-agent -s)"   //ssh-agentを起動
  ssh-add ~/.ssh/id_rsa    
  ssh-add ~/.ssh/**id_ed25519**    //sshのプライベートキーを追加　太字の部分を秘密鍵のファイル名に置き換える
```
### Githubアカウントへの新しいSSHキーの追加
```
  cat /home/riku0202/.ssh/id_ed25519.pub   //公開鍵を表示
 SSHキーをコピー　→　githubのsetting　→　[SSH and GPG keys] → 貼り付ける 
  ssh -T git@github.com    //接続テスト 
  mkdir git  
```
```
  git clone git@github.com:riku0202/til.git    //リモートリポジトリからローカルに複製する 
  cd til
  touch .ignore     //ignoreファイルを作り一部のファイルを除外する
  git status
```
