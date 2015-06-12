# Model - 訂單項

```php
<?php namespace App;

use Illuminate\Database\Eloquent\Model;

class Item extends Model
{
    public function style()
    {
        return $this->hasOne('App\Product');
    }
}
```

