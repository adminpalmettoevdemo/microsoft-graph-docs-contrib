---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SecureScoreControlProfile();
$requestBody->setControlStateUpdates('controlStateUpdates-value');

$result = $graphServiceClient->security()->secureScoreControlProfiles()->bySecureScoreControlProfileId('secureScoreControlProfile-id')->patch($requestBody)->wait();

```