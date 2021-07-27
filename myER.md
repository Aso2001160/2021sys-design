```
@startuml
!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue
entity "顧客マスタ" as customer<m_customers><<M,MASTER_MARK_COLOR>>{
  + customer_code[PK]
  --
  pass
  name
  address
  tel
  mail
  del_flag
  reg_date
}
entity "購入テーブル" as purchase<d_purchase><<T,TRANSACTION_MARK_COLOR>>{
  + order_id[PK]
  --
  customer_code[FK]
  purchase_date
  total_price
}
entity "購入テーブル詳細" as purchase_deta<d_purchase_detail><<T,TRANSACTION_MARK_COLOR>>{
  + detail_id[PK]
  + order_id[PK]
  --
  item_code[FK]
  price
  num
}
entity "商品マスタ" as items<m_items><<M,MASTER_MARK_COLOR>>{
  + item_code[PK]
  --
  item_name
  price
  category_id[FK]
  image
  detail
  del_flag
  reg_date
}


customer|o-r-o{purchase
purchase||-r-|{purchase_deta
purchase_deta}|-d-||items
@enduml
```

