# 數據結構 - 訂單明細

* 明細編號
* 訂單編號
* 產品編號
* 顏色
* 尺寸
* 數量
* 售價

* * *


```php
php artisan make:migration create_items_table --create=items
```

```php
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateItemsTable extends Migration {

        public function up()
        {
                Schema::create('items', function(Blueprint $table)
                {
                        $table->increments('id');
                        $table->integer('order_id');
                        $table->inerger('product_id');
                        $table->string('color');
                        $table->string('size');
                        $table->integer('quantity');
                        $table->integer('price');
                        $table->timestamps();
                });
        }

        public function down()
        {
                Schema::drop('items');
        }

}
```

```php
php artisan migrate
```
