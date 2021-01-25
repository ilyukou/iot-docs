## User Controller
### Request mapping <em>/user</em>

___
### Change sensor state
##### Request /{token}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | - | token | String token - user token from email to confirm account | - | - | - | -

##### Response
Body | Description
------------ | -------------
- | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
404 | Not found User
500 | Internal server error occurred.
