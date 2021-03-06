## Project Controller
### Request mapping <em>/project</em>

___
### Create project
##### Request /project
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
POST | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) |- | - | - | [ProjectForm](https://github.com/ilyukou/iot-docs/tree/main/dto/ProjectForm.md) | - | -

##### Response
Body | Description
------------ | -------------
1 | Long id – ID of created project

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
500 | Internal server error occurred.


___
### Update project
##### Request /project/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
PUT | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of project | - | [ProjectForm](https://github.com/ilyukou/iot-docs/tree/main/dto/ProjectForm.md) | - | -

##### Response
Body | Description
------------ | -------------
 -| -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
403 | Forbidden. Not access for this operation
404 | Not found Project
500 | Internal server error occurred.


___
### Get project
##### Request /project/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of project | - | - | - | -

##### Response
Body | Description
------------ | -------------
[Project](https://github.com/ilyukou/iot-docs/tree/main/dto/Project.md) | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
403 | Forbidden. Not access for this operation
404 | Not found Project
500 | Internal server error occurred.

___
### Get project page
##### Request /project/page?count=1&username=String
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | count, username | int count, String username | username is OPTIONAL field. If not present return your repositories. If present return {username} repositories | - | - | -

##### Response
Body | Description
------------ | -------------
Array of [Project](https://github.com/ilyukou/iot-docs/tree/main/dto/Project.md) | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
500 | Internal server error occurred.

___
### Delete project
##### Request /project/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of project | - | - | - | -

##### Response
Body | Description
------------ | -------------
 -| -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
403 | Forbidden. Not access for this operation
404 | Not found Project
500 | Internal server error occurred.
