# 流程 - 客戶

* 客戶列表
* 新增 
* 檢視客戶資料
* 修改
* 查詢
* 刪除

***

## 新增
```php
Route::get('/customer/new', [ uses' => 'CustomerController@getNew' ]);
Route::post('/customer/new', [ 'uses' => 'CustomerController@postNew' ]);
```