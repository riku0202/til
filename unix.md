# Unix
### Distribution　　　
※配布形式         　  
Ubuntu     
Alpine       
標準的なコマンドは同じ   　　

## コマンド   
date 日時   
cal カレンダー   
ctrl + c 次のコマンドを打つ   
-ls al ディレクトリの中身を見る  
ls --help　　説明
ctrl + u   クリア　
ctrl + L  すべてクリア   
pwd   現在のディレクトリ  
-ls -l 探したいファイルの名前　ワイルドカード   
touch index.html  ファイルを更新ファイルがない場合空ファイルを作る   
cp index.html copy.html ファイルをコピー
mv copy.html aaa.html 名前の変更   
rm aaa.html　　ファイルを削除
mkdir aaa  ディレクトリ作成  
ディレクトリの中身を削除してから削除する   
cp -r aaa　ディレクトリの中身ごとコピー   
cm -r aaa　ディレクトリの中身ごと削除   
cat 中身を見る　　
history 履歴    
!1　さかのぼる    
chmod アクセス権限   
rwxrwxrwx　　
vi ファイル名   viモード    



## ディレクトリ構成   
etc 各種設定ファイル   
var データファイル   
ディレクトリはtabで補完できる

## VIM   
:w 上書き保存   
:w　ファイル名　名前を付けて保存    
:q 終了    
:q! 強制終了      
:e  ほかのファイルを開く     　
gg　先頭に  
G　一番最後に  
ctrl + b　一画面上   
ctrl + f  一画面した  
w　b　単語単位で移動　　
^　行頭  
$　行末  
f + 移動したい単語 　移動したい文字のところまで飛ぶ   
% 対応するかっこに飛ぶ   
v  ビジュアルモード   
V　行単位   
ctrl + v　区系単位　　　
x　カット  
dd　一行カット   
yy　コピー  
検索
//検索  
n　下方向に検索   
N 上方向に選択   
:　コマンドモード   
s/state/State　置換（一つ）  
s/state/State/g　置換（カーソルがある行）   
%/state/State　置換　すべてを置換する   
.　直前の操作を繰り返す   
=  インデントをそろえる  





