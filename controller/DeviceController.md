## Device Controller
### Request mapping <em>/device</em>

___
### Create device
##### Request /device
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
POST | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) |- | - | - | [DeviceForm](https://github.com/ilyukou/iot-docs/tree/main/dto/DeviceForm.md) | - | -

##### Response
Body | Description
------------ | -------------
1 | Long id – ID of created device

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
500 | Internal server error occurred.


___
### Update device
##### Request /device/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
PUT | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of device | - | [DeviceForm](https://github.com/ilyukou/iot-docs/tree/main/dto/DeviceForm.md) | - | -

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
404 | Not found Device
500 | Internal server error occurred.

___
### Get device
##### Request /device/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of device | - | - | - | -

##### Response
Body | Description
------------ | -------------
[Device](https://github.com/ilyukou/iot-docs/tree/main/dto/Device.md) | -

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
### Get devices
##### Request /device?ids=[1,2,3]
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
### Delete device
##### Request /device/{id}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | [User authorization token](https://github.com/ilyukou/iot-docs/tree/main/dto/AuthenticationUser.md) | id | ID of device | - | - | - | -

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
404 | Not found Device
500 | Internal server error occurred.
