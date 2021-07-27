
# MYDB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001160/2021sys-design/blob/main/myER.md)

# DBテーブルカラム詳細一覧

d_purchase
|属性名|型|PK|NN|FK|AI|
|-----|--|--|--|--|--|
|order_id|bigint(20)|〇|〇|-|〇|
|customer_code|varchar(50)|-|〇|-|-|
|purchase_date|date|-|〇|-|-|
|total_price|int(11)|-|〇|-|-|

d_purchase_detail
|属性名|型|PK|NN|FK|AI|DF|
|-----|--|--|--|--|--|--|
|detail_id|bigint(20)|〇|〇|-|〇|-|
|order_id|bigint(20)|〇|-|〇|-|0|
|item_code|int(11)|-|〇|-|-|-|
|price|int(11)|-|〇|-|-|-|
|num|int(11)|-|〇|-|-|-|

m_customers
|属性名|型|PK|NN|FK|DF|
|-----|--|--|--|--|--|
|customer_code|varchar(50)|〇|〇|-||
|pass|varchar(50)|-|〇|-|-|
|name|varchar(20)|-|〇|-|-|
|address|varchar(100)|-|〇|-|-|
|tel|varchar(20)|-|〇|-|-|
|mail|varchar(100)|-|〇|-|-|
|del_flag|int(1)|-|-|-|NULL|
|reg_date|date|-|〇|-|-|

m_items
|属性名|型|PK|NN|FK|DF|
|-----|--|--|--|--|--|
|item_code|int(11)|〇|〇|-|0|
|item_name|varchar(50)|-|〇|-|-|
|price|int(11)|-|〇|-|-|
|image|varchar(200)|-|〇|-|-|
|detail|varchar(500)|-|-|-|NULL|
|del_flag|int(11)|-|-|-|NULL|
|selcount|int(10)|-|-|-|0|
|reg_date|date|-|〇|-|-|
