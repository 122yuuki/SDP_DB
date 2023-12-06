# エラーの解決

エラーが出ている原因の一つとして考えられているのが、今使用しているPCのユーザ名が「***日本語***」であることです。ユーザ名が全角だと、うまくインストールができない場合があります。  

まずは、今のユーザ名を「***半角の英語(空白も半角で!!)***」に直してみる。直したら再実行してみてください。  
それでも同じエラー文が出る場合は、以下の方法で解決してみてください。この方法だと、ほとんどの方が解決できると思います。  

「***設定***」->「***アカウント***」->「***他のユーザー***」->「***アカウントの追加***」でローカルアカウントを作成します。  

<img src="https://github.com/122yuuki/SDP_DB/blob/main/Section_1/img_ano/ano_1.png">  

画像の赤枠をクリックして進んでください。  

<img src="https://github.com/122yuuki/SDP_DB/blob/main/Section_1/img_ano/ano_2.png">  

ユーザー情報を入力するように言われるので、各自入力をしてください。ただし、***ユーザー名を半角英字***で入力してください。  
ユーザーの追加ができたら、「***アカウントの種類の変更***」でアカウントの種類を管理者にして下さい。  

<img src="https://github.com/122yuuki/SDP_DB/blob/main/Section_1/img_ano/ano_3.png">  

___

以上のことが完了したら、戻ってPostgreSQLのインストール(windows)を再度行ってください。  
それでも解決できない場合は、Discordで問い合わせてください。  
___
[目次へ](https://github.com/122yuuki/SDP_DB/blob/main/README.md)

[戻る](https://github.com/122yuuki/SDP_DB/blob/main/Section_1/PostgreSQL_1.md)
