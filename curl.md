curl --version jq command json 形式で出力される

curl localhost://8080/api/json |jq .

curl [オプション]
　-o ファイルの出力する。
　-i http header body の出力をする
-I http header の確認する
-d データを送ることができる　 json 形式で送ることができる
curl -X request /path

# Request

- get
- post
- put
- delete
