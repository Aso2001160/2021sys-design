```uml
@startuml
ユーザー->webサーバー:ログイン
webサーバー->DBサーバー:ログイン照会
DBサーバー->DBサーバー:ログイン処理
DBサーバー->webサーバー:認証結果
@enduml
```