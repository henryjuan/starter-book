# Model - 產品

```php
<?php namespace App;

use Illuminate\Database\Eloquent\Model;

class Product extends Model
{
    public function item()
    {
        return $this->hasOne('App\Item');
    }
}
```

