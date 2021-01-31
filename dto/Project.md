#### Project
Filed name | Type | Note
------------ | ------------- | -------------
id | Long | Project id
sensors | Long array | Sensors ids.
device | Long array | Device ids.
name | String | Project name.
title | Blob | Project title.
owner | Long | [User#id](https://github.com/ilyukou/iot-docs/tree/main/dto/User)

```json
{
    "id" : 1,
    "thing" : {
      "sensor" : [1,2,3],
      "device" : [1,2,3]
    },
    "name" : "String",
    "title" : "Long String",
    "owner" : 1
}

```
