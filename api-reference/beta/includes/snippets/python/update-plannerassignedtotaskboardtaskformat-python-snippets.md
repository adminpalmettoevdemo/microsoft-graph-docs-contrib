---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = PlannerAssignedToTaskBoardTaskFormat(
	order_hints_by_assignee = PlannerOrderHintsByAssignee(
		additional_data = {
				"aaa27244-1db4-476a-a5cb-004607466324" : "8566473P 957764Jk!",
		}
	),
)

request_configuration = AssignedToTaskBoardFormatRequestBuilder.AssignedToTaskBoardFormatRequestBuilderPatchRequestConfiguration()
request_configuration.headers.add("Prefer", "return=representation")
request_configuration.headers.add("If-Match", "W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc=\"")


result = await graph_client.planner.tasks.by_planner_task_id('plannerTask-id').assigned_to_task_board_format.patch(request_body, request_configuration = request_configuration)


```