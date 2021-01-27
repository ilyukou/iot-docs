#### AuthenticationUser
Filed name | Type | Note
------------ | ------------- | -------------
id | Long | [User#id](https://github.com/ilyukou/iot-docs/tree/main/dto/User.md)
username | String | [User#username](https://github.com/ilyukou/iot-docs/tree/main/dto/User.md)
token | String | Authorization token. Dispatched in the request header ("Authorization")
projects | Long array | Array of User [project#id](https://github.com/ilyukou/iot-docs/tree/main/dto/Project.md) ids.

```json
{
    "id" : 1,
    "username" : "String",
    "token" : "String",
    "projects" : [1,2,3]
}

```
