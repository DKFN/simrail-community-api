# Dispatch station timetables

This API will return the timetable of the station post

Source: Official EDR

## Parameters
One of the Post id : `BZ` `LZ_LC` `SG_R52` are the only ones supported during staging

## Request
```
https://staging.simrail.deadlykungfu.ninja/dispatch/BZ
```

## Response
The response will be an Array of StationTimetableRow

```json
[
  {
    "train_number": "14141",
    "train_type": "ECE",
    "type_speed": 0,
    "stop_type": null,
    "platform": " ",
    "arrival_time": "00:00",
    "departure_time": "00:00",
    "from_post": "Dąbrowa Górnicza",
    "to_post": "Sosnowiec Główny",
    "line": "1",
    "start_station": "Warszawa Grochów",
    "terminus_station": "Bohumin",
    "cachedate": "2023-02-12T18:08:32.837Z",
    "hourSort": 0
  },
  {
    "train_number": "41144",
    "train_type": "ECE",
    "type_speed": 0,
    "stop_type": null,
    "platform": " ",
    "arrival_time": "00:05",
    "departure_time": "00:05",
    "from_post": "Sosnowiec Główny",
    "to_post": "Dąbrowa Górnicza",
    "line": "1",
    "start_station": "Bohumin Vrbice",
    "terminus_station": "Warszawa Grochów",
    "cachedate": "2023-02-12T18:08:32.859Z",
    "hourSort": 5
  }
]
```

### StationTimetableRow
| Field            | Type                 | Description                                                |
|------------------|----------------------|------------------------------------------------------------|
| train_number     | `string`             | The number of the train                                    |
| train_type       | `string`             | The type of the train                                      |
| type_speed       | `number / undefined` | The maximum speed for the train type, if we have such info |
| platform         | `string`             | The platform the train will stop. Example `I 1`            |
| arrival_time     | `string`             | Scheduled arrival time of the train                        |
| departure_time   | `string`             | Scheduled departure time of the train                      |
| from_post        | `string`             | The station where the train comes from                     |
| to_post          | `string`             | The station where the train goes                           |
| line             | `string`             | The line the train needs to be sent to                     |
| start_station    | `string`             | The starting station of the train                          |
| terminus_station | `string`             | The terminus station of the train                          |
| cachedate        | `string`             | The last time the data was updated from the source         |
| hourSort         | `ǹumber`             | Internal sorting value, can also help to focus current row |

