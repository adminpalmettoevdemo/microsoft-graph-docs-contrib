---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = PlannerProgressTaskBoardTaskFormat(
	order_hint = "A6673H Ejkl!",
)

request_configuration = ProgressTaskBoardFormatRequestBuilder.ProgressTaskBoardFormatRequestBuilderPatchRequestConfiguration()
request_configuration.headers.add("Prefer", "return=representation")
request_configuration.headers.add("If-Match", "W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc=\"")


result = await graph_client.planner.tasks.by_planner_task_id('plannerTask-id').progress_task_board_format.patch(request_body, request_configuration = request_configuration)


```