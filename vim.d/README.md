
###How to Use .vimrc###
  将来的に、install.vimみたいなものを作る予定です
  base.vimでちょっとは環境構築が楽になるかも…？


1. ホームディレクトリに../cp_to_home/.vimrcを置く
    ホームからvimrcにシンボリックリンクを張る方が好きです

2. neobundle等を導入する
  
  (git needed)
  "ココ、base.vimで自動化できるかも？
  mkdir -p ~/.vim/bundle
  git clone https://github.com/Shougo/neobundle.vim ~/.vim/bundle/neobundle.vim
  git clone https://github.com/Shougo/vimproc ~/.vim/bundle/vimproc

  "ココはvimrcで自動化できているはず
  ~/.vim/bundle/vimproc に入り、make
    環境ごとにコマンドが異なる
    ex:Mac) make -f make_mac_.mak 

3. vimを起動し、:NeobundleInstall

4. enjoy!


###機能について###

  normal:
    tc 等、tab作成に関するnoremap(H,Lでtab移動を含む)
    ,is VimShell起動
    Ctr+a NERDTREE(もう一回押すと閉じる)
    Space f hoge  unite起動(Space f mで最近使ったファイル一覧、等)
 
  insert:
    自動補完、簡易エラーチェック等介護機能搭載
    行番号の左側にいろいろ出ます
    F12で貼り付けモード

###エラーについて###
--colorscheme : colorschemeの設定行を削除or変更

                # ここ自動化したはず 確認できたら消します
                mkdir ~/.vim
                cd ~/.vim
                mkdir colors
                git clone https://github.com/tomasr/molokai
                入っているファイルを、colors直下に


--font(Ricty) : googleで調べて、Rictyを導入
              : brewを使える環境なら、簡単っぽい
             
              参考URL
              最高に見やすいプログラミング用フォントRictyの生成と使い方 - ウェブソク http://news.7zz.jp/font/4390.html #Zenback @gaito777さんから
              : 簡単な方法知ってる人、教えてください
              : 導入できない場合、lightline周りの設定を削除する
               ####で囲まれている！
              :
              
              
              :set guifont=Ricty\ 10 を削除すると、見た目は汚いが使用できる




