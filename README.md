bitcheckpay-php-client
======================

## Execute Example

Write below (as test.php). And run, php test.php

	<?php
	include('bitcheckpay_api.php');
	$API = new jp\bitcheck\pay\BitcheckPay('Your API Key');
	$Data = $API->createInvoice(0.005, 'BTC', 'ItemName');
	if($Data['result'] == 'OK'){
		echo "Done\n";
	}else{
		echo "Fail\n";
		print_r($Data);
	}
	?>

## Doctest

OK case

	$ php test.php
	Done


NG case

	$ php test.php
	Fail
	Array
	(
	    [id] => bcp53fc3fe238f377.73395178
	    [url] =>
	    [status] => invalid
	    [price] => 0.005
	    [currency] => BTC
	    [btcPrice] => 0.005
	    [invoiceTime] =>
	    [expirationTime] =>
	    [currentTime] => 1409040354
	    [result] => NG
	    [error] => APIキーが正しくありません。

	)


## Setting
There is no settings.

## Log
To php's error_log() 
