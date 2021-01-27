## Auth Controller
### Request mapping <em>/auth</em>

___
### Sign In
##### Request /auth/signIn
Method | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
POST | - | - | - | [AuthenticationRequest](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationRequest.md) | - | -

##### Response
Body | Description
------------ | -------------
[AuthenticationUser](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
404 | Not found User
500 | Internal server error occurred.

___
### Sign Up
##### Request /auth/signUp
Method | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
POST | - | - | - | [RegistrationRequest](https://github.com/ilyukou/iot-docs/tree/main/dto/RegistrationRequest.md) | - | -

##### Response
Body | Description
------------ | -------------
[RegistrationResponse](https://github.com/ilyukou/iot-docs/tree/main/dto/RegistrationResponse.md) | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
500 | Internal server error occurred.

___
