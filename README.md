# omniva-magento-2.3

## Before installing

Shop information must be configured.

Depending on whats done with magento might need marketplace.magento.com user to get access tokens for composer. Instructions: https://devdocs.magento.com/guides/v2.3/install-gde/prereq/connect-auth.html

## Installation - FTP **(Step 1)**

Copy `app` folder into magento root folder. Continue with terminal commands.

## Installation - Terminal commands **(Step 2)**


```
composer require setasign/fpdi-tcpdf

php bin/magento setup:upgrade

php -d memory_limit=2G bin/magento setup:di:compile

php -d memory_limit=2G bin/magento setup:static-content:deploy --language lt_LT

php -d memory_limit=2G bin/magento setup:static-content:deploy --language en_US

php bin/magento cache:flush
```

## Configuration **(Step 3)**

Stores -> Configuration, select Sales -> Shipping Methods -> Omniva

Fill in all the required information.