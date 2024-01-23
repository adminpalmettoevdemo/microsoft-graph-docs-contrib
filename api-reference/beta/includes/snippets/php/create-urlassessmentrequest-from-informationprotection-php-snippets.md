---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new UrlAssessmentRequest();
$requestBody->setOdataType('#microsoft.graph.urlAssessmentRequest');
$requestBody->setUrl('http://test.com');
$requestBody->setExpectedAssessment(new ThreatExpectedAssessment('block'));
$requestBody->setCategory(new ThreatCategory('phishing'));

$result = $graphServiceClient->informationProtection()->threatAssessmentRequests()->post($requestBody)->wait();

```