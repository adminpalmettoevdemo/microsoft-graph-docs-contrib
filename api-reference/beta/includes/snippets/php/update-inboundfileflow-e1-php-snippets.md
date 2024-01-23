---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new InboundFileFlow();
$requestBody->setOdataType('#microsoft.graph.industryData.inboundFileFlow');
$requestBody->setDisplayName('Updated flow name');

$result = $graphServiceClient->external()->industryData()->inboundFlows()->byInboundFlowId('inboundFlow-id')->patch($requestBody)->wait();

```