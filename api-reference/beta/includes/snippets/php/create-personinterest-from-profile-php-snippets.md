---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new PersonInterest();
$requestBody->setCategories(['Sports', 	]);
$requestBody->setDescription('World\'s greatest football club');
$requestBody->setDisplayName('Chelsea FC');
$requestBody->setWebUrl('https://www.chelseafc.com');

$result = $graphServiceClient->me()->profile()->interests()->post($requestBody)->wait();

```