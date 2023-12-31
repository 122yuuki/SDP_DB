# Windows版(Macも)

## 1. PostgreSQLの起動  
PostgreSQLのインストールが完了したら、PostgreSQLを起動する。  
「***コマンドプロンプト***(Macはターミナル)」で、  

```
psql -U postgres
```

と入力する。以下の画像のようにパスワードを入力するよう言われるので、インストール時に設定したパスワードを入力してログインする。パスワードを入力する際、入力されたものが反映されていないが、実際には入力できているため入力し終わったらEnterを押下してログインする。　　
ログインができると3・4行目のようなメッセージが出る。  

<img width="500" src="https://github.com/122yuuki/SDP_DB/blob/main/Section_2/sql_db/sql_1.png">

もし、psqlコマンドが使えなかった場合は、[こちら](https://github.com/122yuuki/SDP_DB/blob/main/Section_2/section_2-6.md)から解決するように。 
> [!note]
> `postgres=# `でセミコロン「;」を入力する前にenterを押すと、改行することができる。セミコロンを文末に入力してenterを押すと、クエリが処理される。  

## 2. PostgreSQLの設定
ログインしたら、  

```
postgres=# \l
```

と入力する(「\」が「￥」の場合もある)。そうすると以下の画像のような画面がでる。これは、データベースの一覧表である。  

<img src="https://github.com/122yuuki/SDP_DB/blob/main/Section_2/sql_db/sql_2.png">

データベースを作成するために、以下のように入力する。  

```
postgres=# create database sdp_prmn;
```

`CREATE DATABASE`とメッセージが出るため確認する。  
再び以下のように入力する。  

```
postgres=# \l
```

以下の画面が表示され、「sdp_prmn」というデータベースが確認されたのがわかるだろう。 

<img src="https://github.com/122yuuki/SDP_DB/blob/main/Section_2/sql_db/sql_5.png">

作成したDBに移動するために、以下のように入力する。 

```
postgres=# \c sdp_prmn
```

先ほど「sdp_prmn」DBを作成したが、そのDBに移動したこととなる。

<img width="500" src="https://github.com/122yuuki/SDP_DB/blob/main/Section_2/sql_db/sql_6.png">

## 3. PostgreSQLでテーブル作成
`postgres=# `が`sdp_prmn=# `に変更されていることを確認し、以下のように入力する。  

```
sdp_prmn=# create table 学生情報  (ここで一度Enter)
sdp_prmn-# (id integer, name varchar(10));
```

`CREATE TABLE`とメッセージが出るので確認する。  

正しくテーブルが作成できているかを確認するために、以下のように入力する。  

```
sdp_prmn=# \dt
```

そうすると、以下の画面のように表示され、そこに「学生情報」というテーブルが作成されているだろう。

<img width="500" src="https://github.com/122yuuki/SDP_DB/blob/main/Section_2/sql_db/sql_9.png">

とはいっても、データがないと正しく列が定義されているかわからない。それを確認するために、以下のように入力する。  

```
sdp_prmn=# insert into 学生情報 (ここで一度Enter)
sdp_prmn-# values(10,'千歳太郎'),
sdp_prmn-# (20,'恵庭花子'),
sdp_prmn-# (30,'苫小牧健'),
sdp_prmn-# (40,'札幌丸子');
```

`INSERT 0 4`とメッセージが出るので確認する。データが正しく追加されているかを確認するために、以下のように入力する。  

```
sdp_prmn=# select * from 学生情報;
```

実行結果は画像のようになるはずだ。

<img width="500" src="https://github.com/122yuuki/SDP_DB/blob/main/Section_2/sql_db/sql_11.png">

## 4. テーブルの削除、データベースの削除

4-1. テーブルの削除
以下のように入力すると、テーブルを削除することができる。

```
sdp_prmn=# drop table 学生情報;
```

`DROP TABLE`とメッセージが出るので確認する。    

4-2. データベースの削除
以下のように入力すると、データベースを削除することができる。

```
sdp_prmn=# \c postres
postgres=# drop database sdp_prmn;
```

`DROP DATABASE`とメッセージが出るので確認する。

## 5. その他コマンド

SQLの基礎文法で学んだSQLは、PostgreSQLで使用することができるため、各自確認するように。  
その他PostgreSQLで使用するコマンドについて紹介する。  

| コマンド | 意味 |
|:---:|:---:|
| \l |データベース一覧表示|
| \dn |スキーマ一覧表示|
| \dt |指定のデータベース内のテーブル一覧表示|
| \c スキーマ名 |DBの移動|

これで一通りの動作確認はできたため、戻って練習問題に取り組むように。  

___

[目次へ](https://github.com/122yuuki/SDP_DB/blob/main/README.md)

[戻る](https://github.com/122yuuki/SDP_DB/blob/main/Section_2/section_2-4.md)
