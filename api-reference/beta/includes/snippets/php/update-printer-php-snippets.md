---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Printer();
$requestBody->setName('PrinterName');
$location = new PrinterLocation();
$location->setLatitude(1.1);
$location->setLongitude(2.2);
$location->setAltitudeInMeters(3);
$requestBody->setLocation($location);

$result = $graphServiceClient->escapedPrint()->printers()->byPrinterId('printer-id')->patch($requestBody)->wait();

```