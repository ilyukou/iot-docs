## Thing Controller
### Request mapping <em>/thing</em>
___
### Get thing
##### Request /thing/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of project | - | - | - | -

##### Response
Body | Description
------------ | -------------
Array of [Thing](https://github.com/ilyukou/iot-docs/tree/main/dto/Thing.md) | Sorted array by activity

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
403 | Forbidden. Not access for this operation
404 | Not found Project
500 | Internal server error occurred.
