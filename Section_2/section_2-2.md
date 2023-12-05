# 1．SQLの基本的文法1

よく使うSQLの文法について学習します。  
以下で出てくるワードの解説  

- ***ステートメント*** : 命令の内容や種類を表すことを意味する  
- ***タプル*** : 実データを表す項目の状態  
- ***トランザクション*** : ひとまとまりとして実行されなければならない処理の単位  


## 1-1.DML

DMLとは***Date Manipulation Language***の略称で、データの操作を行うステートメントである。  
主に4つのステートメントをよく使用する。  

| ステートメント名 | 意味 | 使用例 |
| :---: | :---: | :---: |
| INSERT | タプルの追加 |`insert into テーブル名(列名1, 列名2, …) values(列名1のデータ, 列名2のデータ, …);`|
| UPDATE | タプルの更新 |`update テーブル名 set 列名1 = データ, 列名2 = データ, …;`|
| SELECT | タプルの検索 |`select 列名1,列名2, … from テーブル名;`|
| DELET | タプルの削除 |`delete from テーブル名;`|

## 1-2.TCL

TCLとは***Transaction Control Language***の略称で、トランザクションの制御を行うステートメントである。  
主に3つのステートメントをよく使用する。  

| ステートメント名 | 意味 | 使用例 |
| :---: | :---: | :---: |
| BEGIN | トランザクションの開始 |`begin;`|
| COMMIT | トランザクションの完了 |`commit;`|
| ROLLBACK | トランザクションの取消 |`rollback;`|

これらのSQLは、タプルに何かしらの操作を行う際に使用する。  

## 1-3.DDL

DDLとは***Data Define Language***の略称で、データの定義を行うステートメントである。  
主に3つのステートメントをよく使用する。  

| ステートメント名 | 意味 | 使用例 |
| :---: | :---: | :---: |
| CREATE | データ定義の作成 | `create table テーブル名(定義内容);` |
| DROP | データ定義の削除 | `drop table テーブル名;` |
| ALTER | データ定義の変更 | `alter table テーブル名 add column 列名 データ型;` |

※ALTERについて、他にも使用例が複数あるためこちらの[サイト](https://itc.tokyo/sql/alter-table/)を参考に。  

## 1-4.DCL

DCLとは***Data Control Language***の略称で、データの権限を制御するステートメントである。  
主に2つのステートメントをよく使用するが、少し難易度が高い。  

| ステートメント名 | 意味 | 使用例 |
| :---: | :---: | :---: |
| GRANT | ユーザのデータ利用を許可 |`grant 権限1, 権限2, … on データベース.テーブル to ユーザ名;`|
| REVOKE | ユーザのデータ利用許可を取消 |`revoke 権限1, 権限2, … on データベース.テーブル to ユーザ名;`|

この2つのSQLは、頻繁には使用しない。  

## 1-5.データ型

データを扱う際、データにも様々な種類がある。例えば、整数型、実数型、文字列など  
今まで使用してきたプログラム言語と似たものもあるため、すぐに覚えることができるだろう。

| 型名 | キーワード | 意味 |
|:---:|:---:|:---:|
|ブール値型|`boolean`|真偽値(trueやfalse)|
|数値型|`integer`<br>`bigint`<br>`float`<br>`double`|32bit整数<br>64bit整数<br>32bit実数<br>64bit実数|
|連番型|`serial`|integerの連番|
|文字列型|`char`<br>`varchar`|固定長<br>可変長|
|日付・時刻型|`date`<br>`timestamp`|日付<br>日付・時刻|  

> [!注意]
> データが文字列の場合、''(クォーテーション)でデータを囲む必要がある。""(ダブルクォーテーション)では囲めない。

## 1-6.演算子

各自調べなさい。  

___
[目次へ](https://github.com/122yuuki/SDP_DB/blob/main/README.md)  

[前のページ](https://github.com/122yuuki/SDP_DB/blob/main/Section_2/section_2-1.md)

[次のページ](https://github.com/122yuuki/SDP_DB/blob/main/Section_2/section_2-3.md)
