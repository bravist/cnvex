# The [e.cnvex.cn](http://bxapi.cnvex.cn/apiService/intoSchemeService.html) API PHP SDK


## 简介
[企账通2.0](http://www.cnvex.cn/ProductQzt.html) 是重庆汽摩交易所其他企业级交易计算工具，本项目是PHP版本接口实现，官方接口文档参考[这里](http://bxapi.cnvex.cn/apiService/intoSchemeService.html)。目前支持以下功能：
- 微信、支付宝原生APP支付，二维码支付
- 账户余额支付（转账）
- 账户注册、绑定银行卡
- 查询交易记录

扩展包依赖
+ PHP 5.6+
+ GuzzleHttp
+ PHPUnit


## 安装 CNVEX PHP SDK

### 使用[composer](https://getcomposer.org/)
> composer 是php的包管理工具， 通过composer.json里的配置管理依赖的包，同时可以在使用类时自动加载对应的包, 在你的composer.json中添加如下依赖

执行
```
composer require bravist/cnvex
```

使用 Composer 的 autoload 引入
```php
require_once('vendor/autoload.php');
```

使用 Composer 的 autoload 引入
```php
require_once('vendor/autoload.php');
```

### 手动引入
``` php
require_once('/path/to/pingpp-php/init.php');
```


## For Laravel

Add the following line to the section `providers` of `config/app.php`:

```php
'providers' => [
    //...
    Bravist\Cnvex\ServiceProvider::class,
],
```

make configuration:
```
php artisan vendor:publish --provider="Bravist\Cnvex\ServiceProvider"
```

as optional, you can use facade:

```php

'aliases' => [
    //...
    'Cnvex' => Bravist\Cnvex\Facade\Cnvex::class,
		'CnvexSigner' => Bravist\Cnvex\Facade\Signature::class
],
```

support package auto discover on laravel 5.5.

## For Lumen

Add the following line to `bootstrap/app.php` after `// $app->withEloquent();`

```php
...
// $app->withEloquent();

$app->register(Bravist\Cnvex\ServiceProvider::class);
...
```
