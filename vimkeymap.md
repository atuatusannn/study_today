:map nomal and visual
:nmap nomal
:vmap visual
:imap insert
:cmap command mode
:map! insert and command

## keymap 定義の確認
:verbose
:verbose nmap
:verbose imap ...etc

## keymap setting

<> keyboardのkeyに設定する方法
プリフィックスキーをいうものが存在する
ex) <Leader>
let g:mapleader = "\<Space>"

- スペース＋ｗ で保存する
 nnoremap <Leader>w : w<CR>
 space key and w で　w<CR>を実行する nomal node で　再起したくない場合に設定する
 ex)

 imap a : b
 imap c : a
c key 出 aの実行がされて、aはbなので、c -> bになる

inoremapではcはaになるのにできる。