# 數據結構 - 客戶信用評估

* 評估編號
* 評估日期
* 客戶編號
* 評估者
* 信用等級
* 說明

* * *


```php
php artisan make:migration create_assessments_table --create=assessments
```

```php
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateAssessmentsTable extends Migration {

        public function up()
        {
                Schema::create('assessments', function(Blueprint $table)
                {
                        $table->increments('id');
                        $table->date('date');
                        $table->integer('customer_id');
                        $table->string('assessor');
                        $table->integer('credit');
                        $table->text('descrition');
                        $table->timestamps();
                });
        }

        public function down()
        {
                Schema::drop('assessments');
        }

}
```

```php
php artisan migrate
```
