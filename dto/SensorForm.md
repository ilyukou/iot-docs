#### Sensor
Filed name | Type | Note
------------ | ------------- | -------------
project | Long | [Project#id](https://github.com/ilyukou/iot-docs/tree/main/dto/Project.md)
name | String | Sensor name
state | String | Current state. OPTIONAL filed. Default value "off"
states | String array | Array of possible states. OPTIONAL field. Default value "off, on"

```json
{
    "project" : 1,
    "name" : "String",
    "state" : "String",
    "states" : ["String","String"]
}

```
