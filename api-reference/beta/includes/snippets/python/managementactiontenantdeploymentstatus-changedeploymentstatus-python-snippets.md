---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ChangeDeploymentStatusPostRequestBody(
	tenant_group_id = "String",
	tenant_id = "String",
	management_action_id = "String",
	management_template_id = "String",
	status = "String",
)

result = await graph_client.tenant_relationships.managed_tenants.management_action_tenant_deployment_statuses.microsoft_graph_managed_tenant_change_deployment_status.post(request_body = request_body)


```