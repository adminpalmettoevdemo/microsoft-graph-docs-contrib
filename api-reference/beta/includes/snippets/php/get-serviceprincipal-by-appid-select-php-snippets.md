---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new ServicePrincipalsWithAppIdRequestBuilderGetRequestConfiguration();
$queryParameters = ServicePrincipalsWithAppIdRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->select = ["id","appId","displayName","appRoles","publishedPermissionScopes","resourceSpecificApplicationPermissions"];
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->servicePrincipalsWithAppId('{appId}', )->get($requestConfiguration)->wait();

```