# 用例

## 客戶

* 列出客戶
* 新增客戶 
* 檢視客戶資料
* 修改客戶資料
* 查詢客戶
* 刪除客戶資料

***

routes.php

```php
Route::get('/customer/new', [ uses' => 'CustomerController@getNew' ]);
Route::post('/customer/new', [ 'uses' => 'CustomerController@postNew' ]);
```