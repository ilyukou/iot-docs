## Sensor Controller
### Request mapping <em>/sensor</em>

___
### Create sensor
##### Request /sensor
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
POST | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) |- | - | - | [SensorForm](https://github.com/ilyukou/iot-docs/tree/main/dto/SensorForm.md) | - | -

##### Response
Body | Description
------------ | -------------
1 | Long id – ID of created sensor

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
500 | Internal server error occurred.


___
### Update sensor
##### Request /sensor/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
PUT | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of sensor | - | [SensorForm](https://github.com/ilyukou/iot-docs/tree/main/dto/SensorForm.md) | - | -

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
404 | Not found Sensor
500 | Internal server error occurred.

___
### Get sensor
##### Request /sensor/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of sensor | - | - | - | -

##### Response
Body | Description
------------ | -------------
[Sensor](https://github.com/ilyukou/iot-docs/tree/main/dto/Sensor.md) | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
403 | Forbidden. Not access for this operation
404 | Not found Sensor
500 | Internal server error occurred.

___
### Get sensors
##### Request /sensor?ids=[1,2,3]
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | ids | IDs of sensor | - | - | - | -

##### Response
Body | Description
------------ | -------------
Array of [Sensor](https://github.com/ilyukou/iot-docs/tree/main/dto/Sensor.md) | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
403 | Forbidden. Not access for this operation
404 | Not found Sensor
500 | Internal server error occurred.

___
### Delete sensor
##### Request /sensor/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of sensor | - | - | - | -

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
404 | Not found Sensor
500 | Internal server error occurred.
