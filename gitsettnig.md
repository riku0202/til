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

### ubuntuにgolangを入れる方法  
1. ```curl -O https://dl.google.com/go/go1.15.5.linux-amd64.tar.gz```   
		- ubuntu上でこのコマンドを実行し、パッケージを取得する。   
2. ```sudo tar -C /usr/local -xzf go1.15.5.linux-amd64.tar.gz```
		- パッケージを展開して配置する。
3. 一番上のディレクトリへ戻り、.profileを開きPATHを通す
```
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
export PATH=$PATH:/usr/local/go/bin
```
### go mod tidy
### gccを入れる
apt update
### golandの設定変更  
1. Use GOPATH that`s defined in system enviromentのチェックを外す。 
2. project GOPATHの＋を押し、```\\wsl$\Ubuntu-20.04\home\name\go```を指定する。
### ubuntuにgolangを入れる方法  
1. ```curl -O https://dl.google.com/go/go1.15.5.linux-amd64.tar.gz```   
		- ubuntu上でこのコマンドを実行し、パッケージを取得する。   
2. ```sudo tar -C /usr/local -xzf go1.15.5.linux-amd64.tar.gz```
		- パッケージを展開して配置する。
3. 一番上のディレクトリへ戻り、.profileを開きPATHを通す
```
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
export PATH=$PATH:/usr/local/go/bin
export GOPRIVATE=github.com/artis-inc/*  //下の「設定関係」で追記します
```
## 設定関係

- [Golandドキュメント](https://pleiades.io/help/go/meet-the-product.html#first-steps-with-goland)

- [GitHubのプライベートリポジトリをgo getする](https://www.yuyagishita.com/tech/golang/go-get-github-private-repository/)
  - ↓の```export GOPRIVATE```とあわせて
- [Private Modules](https://syfm.hatenablog.com/entry/2019/08/10/170730)

- [Go Modulesでgo.modのGo versionを変更するには](https://qiita.com/hgsgtk/items/a11f56f7db4181311c19)

## goland起動時のエラー
- goland起動時に```go list -m: codehost.WorkDir: can't find or create lock file: Lock```のエラーが発生した場合は、上記にもある通り、以下の1文が```.profile```に記載されていないことを疑う。
```
export GOPRIVATE=github.com/artis-inc/*
```

### golandの設定変更  
1. Use GOPATH that`s defined in system enviromentのチェックを外す。 
2. project GOPATHの＋を押し、```\\wsl$\Ubuntu-20.04\home\name\go```を指定する。
