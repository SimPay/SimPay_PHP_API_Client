# SimPay_PHP_API_Client
Official SimPay.pl PHP API Client 

## Requirements
* PHP 5.3+

## Installation

The SimPay_PHP_API_Client can be installed using [Composer](https://packagist.org/packages/simpay/api_client).

### Composer

Inside of `composer.json` specify the following:

``` json
{
  "require": {
    "simpay/api_client": "dev-master"
  }
}
```

``` php
<?php
// load Composer
require 'vendor/autoload.php';

define('API_KEY', 	'XXXXXXXX');
define('API_SECRET', 	'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX');
define(‘API_VERSION’, 	1);

try {
	
	$api = new SimPay(API_KEY, API_SECRET, API_VERSION);
        $api->getStatus(array(
				'service_id' 	=>	'2',							
				'number'	=>	'7355',
				'code'		=>	'5DB554',						
	));
	
} catch(Exception $e) {
	echo	'Error:	'	.$e->getMessage();
}
	
