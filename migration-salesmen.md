# 數據結構 - 業務員

* 業務編號
* 姓名
* 電話
* Email

* * *


```php
php artisan make:migration create_salesmen_table --create=salesmen
```

```php
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateSalesmenTable extends Migration {

        public function up()
        {
                Schema::create('salesmen', function(Blueprint $table)
                {
                        $table->increments('id');
                        $table->string('name');
                        $table->string('telephone');
                        $table->string('email');
                        $table->timestamps();
                });
        }

        public function down()
        {
                Schema::drop('salesmen');
        }

}
```

```php
php artisan migrate
```
