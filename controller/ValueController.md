## Value Controller
### Request mapping <em>/value</em>

___
### Add new value
##### Request /value/{token}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
POST | - | token | String token - [sensor#token](https://github.com/ilyukou/iot-docs/tree/main/dto/Sensor.md) | - | [Value](https://github.com/ilyukou/iot-docs/tree/main/dto/Value.md) | [Value#time](https://github.com/ilyukou/iot-docs/tree/main/dto/Value.md) is optional field. If not present - server time is set when the request came | -


##### Response
Body | Description
------------ | -------------
-| -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
404 | Not found Sensor with such token
500 | Internal server error occurred.

___
### Get last value
##### Request /value/{token}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | - | token | String token - [sensor#token](https://github.com/ilyukou/iot-docs/tree/main/dto/Sensor.md) | - | [Value](https://github.com/ilyukou/iot-docs/tree/main/dto/Value.md) | - | -


##### Response
Body | Description
------------ | -------------
[Value](https://github.com/ilyukou/iot-docs/tree/main/dto/Value.md) | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
404 | Not found Sensor with such token
500 | Internal server error occurred.

___
### Get value with time filter?from=1&to=2
##### Request /value/period/{token}
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | - | token, from, to | String token - [sensor#token](https://github.com/ilyukou/iot-docs/tree/main/dto/Sensor.md), from - start of time period, to - end of time period | - | - | - | -


##### Response
Body | Description
------------ | -------------
Array of [Value](https://github.com/ilyukou/iot-docs/tree/main/dto/Value.md) | Array size no more than 500

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
404 | Not found Sensor with such token
500 | Internal server error occurred.
