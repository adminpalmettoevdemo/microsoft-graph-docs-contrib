---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$result = $graphServiceClient->identityGovernance()->permissionsAnalytics()->aws()->findings()->byFindingId('finding-id')->get()->wait();

```