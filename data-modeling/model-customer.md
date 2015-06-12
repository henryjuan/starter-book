# Model - 客戶

```php
<?php namespace App\CRM;

use Illuminate\Database\Eloquent\Model;

class Customer extends Model
{
    public function orders()
    {
        return $this->hasMany('App\CRM\Order');
    }

    public function assessments()
    {
        return $this->hasMany('App\CRM\Assessment');
    }

    public function samples()
    {
        return $this->hasMany('App\CRM\Sample');
    }

}
```

