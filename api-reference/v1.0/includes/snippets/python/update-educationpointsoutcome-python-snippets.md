---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = EducationPointsOutcome(
	odata_type = "#microsoft.graph.educationPointsOutcome",
	points = EducationAssignmentPointsGrade(
		odata_type = "#microsoft.graph.educationAssignmentPointsGrade",
		points = 85.0,
	),
)

result = await graph_client.education.classes.by_classe_id('educationClass-id').assignments.by_assignment_id('educationAssignment-id').submissions.by_submission_id('educationSubmission-id').outcomes.by_outcome_id('educationOutcome-id').patch(request_body = request_body)


```