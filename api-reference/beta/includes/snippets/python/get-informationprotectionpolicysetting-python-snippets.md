---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.users.by_user_id('user-id').security.information_protection.label_policy_settings.get()


```