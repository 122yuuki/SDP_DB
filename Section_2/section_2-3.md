# 2．SQLの基本部文法2

前ページのSQLだけでは高度なデータ操作をすることができないため、より具体的なSQLについて紹介する。  
以降で使用するテーブルは、この2つに限定する。  

<img width="500" src="https://github.com/122yuuki/SDP_DB/blob/main/Section_2/DB_%E3%83%86%E3%83%BC%E3%83%96%E3%83%AB%E4%BE%8B.png">
<img width="250" src="https://github.com/122yuuki/SDP_DB/blob/main/Section_2/DB_%E3%83%86%E3%83%BC%E3%83%96%E3%83%AB%E4%BE%8B2.png">  

## 2-1.where句, order by句

1．「***where句***」は、特定のカラム(列)もしくはタプル(組)を操作させるときに使用する。  

使い方 : ` where 条件式; `

例 1: 
```
select 学籍番号 from 学生情報
  where クラス = 'A';
```
実行結果 : 
| 学籍番号 |
|:---:|
|b1990000|
|b1990050|

例 2:
```
select 学籍番号 from 学生情報
  where 出席番号 > 10 and 出席番号 < 40;
```
実行結果 : 
| 学籍番号 |
|:---:|
|b1990010|
|b1990020|
|b1990030|
|b1990040|  

2．「***order by句***」とは、出力結果のタプルの順番を降順もしくは昇順に並べ替えるときに使用する。
`asc`：昇順  
`desc`：降順  

使い方 : ` order by 列名 ascまたはdesc;` 

例 1:
```
select 学籍番号 from 学生情報
  where 出席番号 > 10 and 出席番号 < 40
  order by 出席番号 asc;
```

## 2-2.





___
[目次へ](https://github.com/122yuuki/SDP_DB/blob/main/README.md)  

[前のページ](https://github.com/122yuuki/SDP_DB/blob/main/Section_2/section_2-2.md)  

[次のページ](https://github.com/122yuuki/SDP_DB/blob/main/Section_2/section_2-4.md)
