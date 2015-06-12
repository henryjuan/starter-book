# Model - 訂單

```php
<?php namespace App\CRM;

use Illuminate\Database\Eloquent\Model;

class Order extends Model
{
    public function customer()
    {
        return $this->belongsTo('App\CRM\Customer');
    }

	publuc function salesman()
	{
		return $this->belogsTo('App\CRM\Salesman');
	}

    public function items()
    {
        return $this->hasMany('App\CRM\Item');
    }
}
```

