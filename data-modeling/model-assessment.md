# Model - 信用評估

```php
<?php namespace App\CRM;

use Illuminate\Database\Eloquent\Model;

class Assessment extends Model
{
    public function customer()
    {
        return $this->belongsTo('App\CRM\Customer');
    }
}
```

