---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SendVirtualAppointmentSmsPostRequestBody();
$additionalData = [
	'phoneNumbers' => [
'+13129224122', '+1242421412', ],
	'virtualAppointmentSmsType' => 'confirmation',
];
$requestBody->setAdditionalData($additionalData);

$graphServiceClient->me()->onlineMeetings()->byOnlineMeetingId('onlineMeeting-id')->sendVirtualAppointmentSms()->post($requestBody)->wait();

```