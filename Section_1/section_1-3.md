# 2．SQLとは何か

前ページで紹介したが、DBを操作するために必要なものとして「***クエリ***」という問い合わせ文がある。例として`select`を使ったが、その他にも`delete`や`update`といったクエリがある。  

関係データベース(以下RDB)で利用できるクエリの形式として「***SQL***(エスキューエルやシークェルなどと呼ぶ)」というものがある。DBMS上でデータやデータベースを制御するための言語であり、ユーザーやシステムからの命令を受けてRDBにクエリを行い結果を返す。  
SQLにも種類があり、***MySQL***や***PostgreSQL***といったオープンソース、Oracle社のOracle Database、Microsoft社のMicrosoft SQL ServerやAccessなどがあるが、将来性を考えて今回はPostgreSQLを使ってDBについて学習する。  
SQLの具体的な操作方法・文法は次回セクションで学習する。  

<img width="700" src="https://github.com/122yuuki/SDP_DB/blob/main/Section_1/DB_%E3%82%AF%E3%82%A8%E3%83%AA%E8%AA%AC%E6%98%8E%E5%9B%B3.png">  

## 2-1.PostgreSQLとは何か

PostgreSQL(以下ポスグレ)とは、オープンソースソフトウェアのデータベース言語であり、***リレーショナルデータベース管理システム***(RDBMS)である。  
ポスグレは、標準SQLの大半に準拠、さらに標準SQLを拡張しているため、高品質のシステム開発をすることが可能。そのため、多くの企業でポスグレが採用されている。

<img width="500" src="https://github.com/122yuuki/SDP_DB/blob/main/Section_1/PostgreSQL_%E5%9B%B3.png">  

## 2-2.PostgreSQLのインストール

以降の演習問題では、PostgreSQLを使って問題に取り組んでもらうため、以下のリンクにアクセスしてPostgreSQLをインストールしてください。  
-> [PostgreSQLをインストールする](https://github.com/122yuuki/SDP_DB/blob/main/Section_1/ready.md)  

## 補足 : 関係データベースとは？？
関係データベース(RDB)とは、データを表形式で扱っているデータベースのことである。(リレーショナルデータベースともいう)  
複数の表(テーブル)を合成することも可能である。より柔軟にデータを管理するためには大切なデータベースである。

___

[目次](https://github.com/122yuuki/SDP_DB/tree/main#readme)  

[前のページ](https://github.com/122yuuki/SDP_DB/blob/main/Section_1/section_1-2.md)  
