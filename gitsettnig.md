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

* 200  ssh-keygen -t ed25519 -C "riku0202excalibur@gmail.com"   //メールアドレスをラベルとしてSSHキーを作成
* 201  cd.ssh
* 202  eval "$(ssh-agent -s)"   //ssh-agentを起動
* 203  ssh-add ~/.ssh/id_rsa    
* 204  ssh-add ~/.ssh/**id_ed25519**    //sshのプライベートキーを追加　太字の部分を秘密鍵のファイル名に置き換える
* 205  cat /home/riku0202/.ssh/id_ed25519.pub   //公開鍵を表示
* 206  ssh -T git@github.com    //接続テスト
* 207  ll
* 208  mkdir git  
* 209  ll
* 210  cd git
* 211  git clone git@github.com:riku0202/til.git    //リモートリポジトリからローカルに複製する
* 212  ll
* 213  cd till
* 214  cd til
* 215  ll
* 216  git log
* 217  git status
* 218  touch .ignore
* 219  git status
* 220  add aa.md
* 221  git add .
* 222  git commit -m"aa"
* 223  git log
* 224  git brach
* 225  git branch
* 226  git push origin main
* 227  git pull origin main
* 228  cd ../
* 229  ll
* 230  git init
* 231  git add C:\Users\riku-s\tour of go
* 232  ll
* 233  cd tour_of_go/
* 234  ll
* 235  git init
* 236  ll
* 237  git add .
* 238  git commit -m a
* 239  git log
* 240  git branch
* 241  git branch -M main
* 242  git branch
* 243  git remote add origin git@github.com:riku0202/tour_of_go.git
* 244  git push -u origin main
* 245  cd ../
* 246  ll
* 247  cd practice/
* 248  ll
* 249  git init
* 250  git commit -m
* 251  git commit -m a
* 252  git init
* 253  git commit -m aaa
* 254  ll
* 255  git commit -m"a"
* 256  git remote add origin git@github.com:riku0202/practice_airtis.git
* 257  git push -u origin main
* 258  git commit -m k
* 259  git branch
* 260  git branch
* 261  ll
* 262  git branch
* 263  git init
* 264  git log
* 265  git status
* 266  git add .
* 267  git status
* 268  git rm --cached .idea/awesomeProject.iml
* 269  git status
* 270  git rm --cached .idea/modules.xml
* 271  git rm --cached .idea/workspace.xml
* 272  git status
* 273  touch .gitignore
* 274  vim .gitignore
* 275  ll
* 276  git status
* 277  git add .
* 278  git status
* 279  git commit -m a
* 280  git branch
* 281  git branch -M main
* 282  git branch
* 283  git remote add origin git@github.com:riku0202/practice_airtis.git
* 284  git push -u origin main
* 285  cd
* 286  cd git
* 287  ll
* 288  cd til
* 289  git remote add origin git@github.com:riku0202/til
* 290  git remote rm origin
* 291  git remote add origin git@github.com:riku0202/til
* 292  git add .
* 293  git commit -m change
* 294  git commit -mchange
* 295  git status
* 296  git branch
* 297  git add .
* 298  git commit -m"change"
* 299  git add .
* 300  git commit -m"change"
* 301  ll
* 302  git push origin main
* 303  git status
* 304  git log
* 305  git push origin main
* 306  git add .
* 307  git commit -m"change"
* 308  git push origin main
* 309  git commit -m"change"
* 310  git push origin main
* 311  git add .
* 312  git commit -m"change"
* 313  git push origin main
* 314  history