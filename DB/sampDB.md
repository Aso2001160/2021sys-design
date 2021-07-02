### DB設計書

d_purchase
|属性名|型|PK|NN|FK|AI|
|-----|--|--|--|--|--|
|order_id|bigint(20)|〇|〇|-|〇|
|customer_code|varchar(50)|-|〇|-|-|
|purchase_date|date|-|〇|-|-|
|total_price|int(11)|-|〇|-|-|

d_purchase_detail
