# 購入テーブル 
**d_purchase**
|属性名|型|PK|FK|NN|
|:------|:-----|:--|:--|:--|
|order_id|bigint(20)|○||○|
|customer_code|varchar(50)|||○|
|purchase_date|date|||○|
|total_price|int(11)|||○|
 
# 購入テーブル詳細
**d_purchase_detail**
|属性名|型|PK|FK|NN|
|:------|:-----|:--|:--|:--|
|detail_id|bigint(20)|○||○|
|order_id|bigint(20)|○|○|○|
|item_code|int(11)|||○|
|price|int(11)|||○|
|num|int(11)|||○|

# ユーザー（顧客）テーブル
**m_customers**
|属性名|型|PK|FK|NN|
|:------|:-----|:--|:--|:--|
|customer_code|varchar(50)|○||○|
|pass|varchar(50)|||○|
|name|varchar(20)|||○|
|address|varchar(100)|||○|
|tel|varchar(20)|||○| 
|mail|varchar(100)|||○|
|del_flag|int(1)|||○|
|eg_date|date|||○|

# カテゴリテーブル
**m_category**
|属性名|型|PK|FK|NN|
|:------|:-----|:--|:--|:--|
|category_id|int(11)|○||○|
|name|varchar(20)|||○|
|reg_date|date|||○|

# 商品テーブル
**m_items**
|属性名|型|PK|FK|NN|
|:------|:-----|:--|:--|:--|
|item_code|int(11)|○||○| 
|item_name|varchar(50)|||○| 
|price|int(11)|||○| 
|category_id|int(11)||○|○| 
|image|varchar(200)|||○| 
|detail|varchar(500)|||○| 
|del_flag|int(11)|||○| 
|reg_date|date|||○|
