## Sensor State Controller
### Request mapping <em>/sensorState</em>

___
### Create sensor
##### Request /sensorState/{token}?currentState=yourState
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET | - | currentState | String currentState - device state, default "off" | - | - | - | -

If currentState not equals state in server - return state from server, else wait 30 second (each second take fresh data from the server and compare it again). After 30 second return TimeOutMessage.

##### Response when currentState not equals state in server
Body | Description
------------ | -------------
[HttpMessageWrapper < SensorState >](https://github.com/ilyukou/iot-docs/dto/SensorHttpMessageWrapper) | T body [SensorState](https://github.com/ilyukou/iot-docs/dto/SensorState), HttpMessageWrapper#status - 'ok', HttpMessageWrapper#message - "ok"

##### Response when currentState not equals state in server
Body | Description
------------ | -------------
[HttpMessageWrapper < empty >](https://github.com/ilyukou/iot-docs/dto/SensorHttpMessageWrapper) | T body - empty, HttpMessageWrapper#status - 'info', HttpMessageWrapper#message - "Time Out."

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
500 | Internal server error occurred.

___
### Change sensor state
##### Request /sensorState/{token}?state=yourState
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
PUT | - | state | String state - new state | - | - | - | -

##### Response
Body | Description
------------ | -------------
- | -

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
401 | Unauthorized
500 | Internal server error occurred.
