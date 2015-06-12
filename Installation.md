# 準備開發環境

## 安裝 Laravel
```php
composer global require "laravel/installer=~1.1"
```

## 建立專案
```php
laravel new crm
```

## 建立 Models 目錄
```
mkdir app/CRM
```

## 環境設定
修改 .env
```
APP_ENV=local
APP_DEBUG=true
APP_KEY=ChCWtF6xTHf8heFo06ppccK7fxZ93v7a

DB_HOST=localhost
DB_DATABASE=CRM
DB_USERNAME=CRM
DB_PASSWORD=secret

CACHE_DRIVER=file
SESSION_DRIVER=file
QUEUE_DRIVER=sync

MAIL_DRIVER=smtp
MAIL_HOST=mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
```
