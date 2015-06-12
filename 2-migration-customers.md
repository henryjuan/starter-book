# 數據結構 - 客戶

* 客戶編號
* 客戶名稱
* 公司地址
* 公司電話
* 聯絡人姓名
* Email

* * *


```php
php artisan make:migration create_customers_table --create=customers
```

```php
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateCustomersTable extends Migration {

        public function up()
        {
                Schema::create('customers', function(Blueprint $table)
                {
                        $table->increments('id');
                        $table->string('name');
                        $table->string('address');
                        $table->string('telephone');
                        $table->string('contact');
                        $table->string('email');
                        $table->text('memo');
                        $table->timestamps();
                });
        }

        public function down()
        {
                Schema::drop('customers');
        }

}
```

```php
php artisan migrate
```
