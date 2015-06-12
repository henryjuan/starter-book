# 資料塑模

## 建立 Entities

* User (用戶)
* Customer (客戶)
* Style (款式)
* Order (訂單)
* Item (訂單項)
* Sample (樣品)
* Assessment (客戶信用評估)
* Factory (工廠)
* Salesman (業務)

## 客戶

```php
php artisan make:model CRM/Customer
```

## 產品

```php
php artisan make:model CRM/Style
```

## 訂單

```php
php artisan make:model CRM/Order
```
## 訂單明細

```php
php artisan make:model CRM/Item
```

## 樣品

```php
php artisan make:model CRM/Sample
```

## 工廠

```php
php artisan make:model CRM/Factory
```

## 評估
```php
php artisan make:model CRM/Assessment
```