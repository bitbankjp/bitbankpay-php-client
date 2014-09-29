bitbankpay-php-client
======================

Examples
--------

### createInvoice

```php
include('./bitbankpay_api.php');
use jp\bitbank\pay\BitbankPay;

$bitcheckPay = new BitbankPay('API Key');
$bitcheckPay->setOrderID('order_id');
$bitcheckPay->setUserMail('mail');
$json = $bitcheckPay->createInvoice(amount,'currency','item_name');
```

### acceptJpyYen

```php
$bitcheckPay->acceptJpyYen($json['id']);
```
### acceptBitcoin

```php
$bitcheckPay->acceptBitcoin($json['id']);
```