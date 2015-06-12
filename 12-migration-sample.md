# 數據結構 - 樣品

* 樣品編號
* 打樣日期
* 工廠
* 打樣費用
* 客戶編號
* 照片
* 類別

* * *


```php
php artisan make:migration create_products_table --create=products
```

```php
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateSamplesTable extends Migration {

        public function up()
        {
                Schema::create('samples', function(Blueprint $table)
                {
                        $table->increments('id');
                        $table->date('date');
                        $table->interger('factory_id');
                        $table->float('cost');
                        $table->integer('customer_id');
                        $table->integer('photo_path');
                        $table->timestamps();
                });
        }

        public function down()
        {
                Schema::drop('samples');
        }

}
```

```php
php artisan migrate
```
