# 數據結構 - 工廠

* 工廠編號
* 工廠名稱
* 地址
* 電話
* Email
* 負責人
* 類別

* * *


```php
php artisan make:migration create_factories_table --create=factories
```

```php
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateFactoriesTable extends Migration {

        public function up()
        {
                Schema::create('products', function(Blueprint $table)
                {
                        $table->increments('id');
                        $table->string('name');
                        $table->string('address');
                        $table->string('telephone');
                        $table->string('fax');
                        $table->string('email');
                        $table->text('description');
                        $table->timestamps();
                });
        }

        public function down()
        {
                Schema::drop('factories');
        }

}
```

```php
php artisan migrate
```
