# Train Timetable API

This API retrieves the train schedules for a driver given a train number

```
https://staging.simrail.deadlykungfu.ninja/train/40684
```

## Response
Will return an array of TrainTimetableRow
```json
[
  {
    "train_number": "40684",
    "scheduled_arrival_hour": null,
    "station": "Tychy Lodowisko",
    "layover": null,
    "scheduled_departure_hour": "17:26",
    "train_type": "ROJ",
    "line": "179",
    "cachedate": "2023-02-12T18:48:23.975Z",
    "stop_type": "ph",
    "hourSort": 0
  },
  {
    "train_number": "40684",
    "scheduled_arrival_hour": "17:27",
    "station": "Tychy Miasto",
    "layover": "0.0",
    "scheduled_departure_hour": "17:27",
    "train_type": "ROJ",
    "line": "179",
    "cachedate": "2023-02-12T18:48:24.000Z",
    "stop_type": null,
    "hourSort": 1727
  }
]
```

## TimeTableRow

| Field                  | Type            | Description                                                              |
|------------------------|-----------------|--------------------------------------------------------------------------|
| train_number           | `string`        | The number of the train                                                  |
| scheduled_arrival_hour | `string / null` | The time the train should arrive at the station                          |
| station                | `string`        | The station name                                                         |
| layover                | `string / null` | Time in minutes of the layover if the train stops at this station        |
| line                   | `string`        | The line the train will be running at this station                       |
| cachedate              | `string`        | Time this data was updated for the last time                             |
| stop_type              | `string / null` | If there is a stop at the station, the type of the layover. `ph` or `pt` |