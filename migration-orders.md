# 數據結構 - 訂單

* 訂單編號
* 客戶訂單號碼
* 客戶編號
* 業務員編號
* 訂單金額
* 訂單日期
* 出貨期
* 交貨日期
* 付款方式

***

```php
php artisan make:migration create_orders_table --create=orders
```

```php
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateOrdersTable extends Migration {

        public function up()
        {
                Schema::create('orders', function(Blueprint $table)
                {
                        $table->increments('id');
                        $table->string('ref');
                        $table->string('customer_id');
                        $table->string('salesman_id');
                        $table->integer('amount');
                        $table->date('order_date');
                        $table->integer('shipping_window_days');
                        $table->date('shipping_date');
                        $table->string('payment');
                        $table->timestamps();
                });
        }

        public function down()
        {
                Schema::drop('orders');
        }

}
```

```php
php artisan migrate
```
