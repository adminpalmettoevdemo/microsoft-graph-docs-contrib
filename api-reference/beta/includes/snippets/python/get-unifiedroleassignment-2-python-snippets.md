---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = UnifiedRoleAssignmentItemRequestBuilder.UnifiedRoleAssignmentItemRequestBuilderGetQueryParameters(
		expand = ["roleDefinition"],
)

request_configuration = UnifiedRoleAssignmentItemRequestBuilder.UnifiedRoleAssignmentItemRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.role_management.directory.role_assignments.by_unified_role_assignment_id('unifiedRoleAssignment-id').get(request_configuration = request_configuration)


```