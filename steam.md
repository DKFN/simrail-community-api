# Steam profiles

Returns the username and the avatarUrl of a given user without calling SimRail API and cached for a day

## Request
```
https://staging.simrail.deadlykungfu.ninja/steam/<steam_id>
```

## Response
An array containing one object with the data

```json
[
  {
    "avatar": "https://avatars.akamai.steamstatic.com/70845eef7475441ffc0c9f9685cf40a57df07e15.jpg",
    "pseudo": "Someone"
  }
]
```
