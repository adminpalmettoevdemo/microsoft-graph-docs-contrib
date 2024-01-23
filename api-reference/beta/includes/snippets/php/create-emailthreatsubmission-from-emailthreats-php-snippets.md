---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EmailUrlThreatSubmission();
$requestBody->setOdataType('#microsoft.graph.security.emailUrlThreatSubmission');
$requestBody->setCategory(new SubmissionCategory('spam'));
$requestBody->setRecipientEmailAddress('tifc@a830edad9050849EQTPWBJZXODQ.onmicrosoft.com');
$requestBody->setMessageUrl('https://graph.microsoft.com/beta/users/c52ce8db-3e4b-4181-93c4-7d6b6bffaf60/messages/AAMkADU3MWUxOTU0LWNlOTEt=');

$result = $graphServiceClient->security()->threatSubmission()->emailThreats()->post($requestBody)->wait();

```