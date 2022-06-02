## ユーザ種類　/etc/passwd file はお s が使用するので基本的に内容の編集は NG です。

    root
    一般ユーザ

ユーザを新規作成
ex) useradd testuser

su [オプション]　引数
su - root (userName)

id 引数
$ id testuser
uid = userID gid= groupID ...etc

usermod,userdel(ユーザを削除する command)

グループごとに権限を指定できる　/etc/group file に書いてある

- プライマリーグループ
- サブグループ

groupadd,groupdel

permission : アクセス権のこと　 r w x -xxxyyyzzz で表記される

chmod でパーミッションに変更することができる
chown オーナを変更できる
ex) chown testuser ./file1
chgrp ファイル、ディレクトリのグループを変更することが出来る
ex) chgrp root ./file1 file1 は root グループに変更されて、root ユーザしか操作できない file ができる。

## ネットワークインターフェース設定ファイル　------------------------

IP アドレス、サブネットマスク、デフォルトデートウェイなどの設定が行えます。root だけが行うことができる

# 　この設定ファイルは編集するのはリスクがある

/etc/syscnfig/network-scripts/ifcfg.....

divece デバイス名
onboot ネットワーク通信できるかどうか
bootproto IP アドレスの設定方法の指定
ipaddr IP アドレス
netmask サブネットマスク
gateway デフォルトデートウェイ
dns1 DNS サーバの IP アドレス

# そこで！

nmtui を利用する

## command

- ip ex) ip addr show
- /etc/resolv.conf file 名前解決をする DNS サーバの設定ファイル DNS
- ifconfig ネットワークインタフェースを管理する。
- ping 通信疎通確認する。
- ssh リモートログインする。
- who login user を確認できる -



## サーバ構築　linux serveer状にミドルウェア(ubuntu,centos)をインストールし、サービスを提供できるようにすること。

1. パッケージのインストール
2. パッケージを起動し、プロセス化
3. コンテンツ作成
4. 設定ファイルの編集し、公開範囲の変更
5. サービスの再起動で、5の変更を反映
6. ファイアウォールや権限の設定



