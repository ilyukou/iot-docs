## Search Controller
### Request mapping <em>/search</em>

___
### Find public project via query
##### Request /search?query=yourQuery
Method | Header | Parameter | Description | Restriction | Body | Description | Restriction
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
GET |- | query | String query - text query | - | - | - | -

##### Response
Body | Description
------------ | -------------
[1,2,3] | List of [Project](https://github.com/ilyukou/iot-docs/dto/Project) id

##### Response Code
Code | Description
------------ | -------------
200 | OK
400 | Validation error or request body is an invalid JSON or cannot be parsed
500 | Internal server error occurred.
