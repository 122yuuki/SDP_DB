# Windows版

## 1.PostgreSQLの起動  

PostgreSQLのインストールが完了したら、PostgreSQLを起動する。  
「***コマンドプロンプト***」で、`psql -U Postgres`と打ち込む。すると、以下の画像のようにパスワードを入力するよう言われるので、インストール時に設定したパスワードを入力してログインする。 
ログインが出ると3・4行目のようなメッセージが出る。  

<img src="">

もし、psqlコマンドが使えなかった場合は、[こちら](https://github.com/122yuuki/SDP_DB/blob/main/Section_2/section_2-6.md)から解決するように。 
> [!note]
> `postgres=# `でセミコロン「;」を入力する前にenterを押すと、改行することができる。セミコロンを文末に入力してenterを押すと、クエリが処理される。  

## 2.PostgreSQLの設定

ログインしたら、

```
postgres=# \n
```

と入力する(「\」が「￥」の場合もある)。そうすると以下の画像のような画面がでる。これは、データベースの一覧表である。  

<img src="">

データベースを作成するために、

```
postgres=# creat database sdp_prmn;
```

と入力する。再び

```
postgres=# \n
```

と入力すると、以下の画面が表示され、「sdp_prmn」というデータベースが確認されたのがわかるだろう。  
<img src="">

作成したデータベースのスキーマーに移動するために、

```
postgres=# 
```

___

[目次へ](https://github.com/122yuuki/SDP_DB/blob/main/README.md)

[戻る](https://github.com/122yuuki/SDP_DB/blob/main/Section_2/section_2-4.md)
