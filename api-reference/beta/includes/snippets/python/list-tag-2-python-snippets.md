---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.compliance.ediscovery.cases.by_case_id('case-id').tags.by_tag_id('tag-id').child_tags.get()


```