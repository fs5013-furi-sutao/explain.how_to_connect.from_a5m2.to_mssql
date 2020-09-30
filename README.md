# a5m2 から SQL Server (mssql) への接続設定
a5m2 から SQL Server (mssql) に接続設定をして、接続確認をするまでの手順を説明する。

## SQL Server の準備
SQL Server を手軽に試したい場合は、以下の手順で DB コンテナを用意、起動しておく。

SQL Server コンテナの docker-compose 構成サンプル:  
https://github.com/fs5013-furi-sutao/mssql.server.linux

## SQL Server (mssql) 拡張のインストー
a5m2 を開く。

サイドバーから「データベース」を右クリックして、メニューから「データベースの追加と削除」を選択する。

![](./add_remove_database.a5m2.png)

「データベースの追加と削除」ウィンドウが開いたら、「追加」ボタンをクリック。

![](./add_db_button.a5m2.png)

「接続タイプの選択」ウィンドウでは、「Microsoft SQL Server」を選択。

接続設定には以下のように環境に合わせて値を登録していく。

![](./registerd_db_settings.a5m2.png)

接続設定例:
```yaml
接続タイプ: SQL Server
サーバー名: 192.168.99.100
ポート番号: 1433
認証方法: SQL Server 認証を使用する
ユーザーID: sa
パスワード: msSqlserver123
データベース名: EmployeeDb
```

設定値があっているか一度、



## 接続設定の追加
開いた SQL Server ペインから + Add Connection をクリックする。

コマンドパレットが開き、接続設定の入力を求められるので、各設定項目を順番に入力していく。


## テーブルのレコードを見る
左部ペインから対象のテーブルを右クリックすると以下のイメージの通り「Select Top 1000」と表示される
![](./connected_with_mssql.png)
