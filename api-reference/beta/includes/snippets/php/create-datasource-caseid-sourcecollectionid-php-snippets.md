---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new UserSource();
$requestBody->setOdataType('microsoft.graph.ediscovery.userSource');
$requestBody->setEmail('badguy@contoso.com');

$result = $graphServiceClient->compliance()->ediscovery()->cases()->byCaseId('case-id')->sourceCollections()->bySourceCollectionId('sourceCollection-id')->additionalSources()->post($requestBody)->wait();

```