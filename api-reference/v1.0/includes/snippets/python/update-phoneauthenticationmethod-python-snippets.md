---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = PhoneAuthenticationMethod(
	phone_number = "+1 2065555554",
	phone_type = AuthenticationPhoneType.Mobile,
)

result = await graph_client.users.by_user_id('user-id').authentication.phone_methods.by_phone_authentication_method_id('phoneAuthenticationMethod-id').patch(request_body)


```