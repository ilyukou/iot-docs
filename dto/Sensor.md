#### Sensor
Filed name | Type | Note
------------ | ------------- | -------------
id | Long | Sensor id
project | Long | [Project#id](https://github.com/ilyukou/iot-docs/tree/main/dto/Project.md)
name | String | Sensor name
state | String | Current state
states | String array | Array of possible states
token | String | Sensor token

```json
{
    "id" : 1,
    "project" : 1,
    "name" : "String",
    "state" : "String",
    "states" : ["String","String"],
    "token" : "String"
}

```
