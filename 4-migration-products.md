# 數據結構 - 產品

* 產品編號
* 產品名稱
* 定價
* 產品照片
* 產品說明

* * *


```php
php artisan make:migration create_products_table --create=products
```

```php
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateProductsTable extends Migration {

        public function up()
        {
                Schema::create('products', function(Blueprint $table)
                {
                        $table->increments('id');
                        $table->string('name');
                        $table->string('price');
                        $table->binary('photo');
                        $table->text('description');
                        $table->timestamps();
                });
        }

        public function down()
        {
                Schema::drop('products');
        }

}
```

```php
php artisan migrate
```
