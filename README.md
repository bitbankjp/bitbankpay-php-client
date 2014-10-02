bitbankpay-php-client
======================

Examples
--------

### createInvoice

```php
include('./bitbankpay_api.php');
use jp\bitbank\pay\BitbankPay;

$bitbankPay = new BitbankPay('API Key');
$bitbankPay->setOrderID('order_id');
$bitbankPay->setUserMail('mail');
$json = $bitbankPay->createInvoice(amount,'currency','item_name');
```

### acceptJpyYen

```php
$bitbankPay->acceptJpyYen($json['id']);
```
### acceptBitcoin

```php
$bitbankPay->acceptBitcoin($json['id']);
```