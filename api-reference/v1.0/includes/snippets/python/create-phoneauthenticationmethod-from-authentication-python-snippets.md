---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = PhoneAuthenticationMethod(
	phone_number = "+1 2065555555",
	phone_type = AuthenticationPhoneType.Mobile,
)

result = await graph_client.users.by_user_id('user-id').authentication.phone_methods.post(request_body = request_body)


```