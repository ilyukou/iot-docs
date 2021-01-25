## Auth Controller
### Request mapping <em>/auth</em>

___
### Sign In
##### Request /auth/signIn
Method | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
POST | - | - | - | [AuthenticationRequest](https://github.com/ilyukou/iot-docs/dto/AuthenticationRequest) | - | -

##### Response
Body | Description
------------ | -------------
[AuthenticationUser](https://github.com/ilyukou/iot-docs/dto/AuthenticationUser) | -

___
### Sign Up
##### Request /auth/signUp
Method | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
POST | - | - | - | [RegistrationRequest](https://github.com/ilyukou/iot-docs/dto/RegistrationRequest) | - | -

##### Response
Body | Description
------------ | -------------
[RegistrationResponse](https://github.com/ilyukou/iot-docs/dto/RegistrationResponse) | -

___
