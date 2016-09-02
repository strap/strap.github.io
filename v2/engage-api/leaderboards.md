---
title: "Leaderboards"
excerpt: ""
---
### GET /api/leaderboard/{slug}/{date}
The leaderboard route will return the list of all leaderboards, a challenge's leaderboards by the optional **slug** parameter, or a challenge's leaderboard by the optional **date** (format: YYYY-MM-DD) parameter.

*All Leaderboards Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/leaderboard"
```
<br>
*All Leaderboards Response*
```json
[
    {
        "slug": "test_daily",
        "period": "daily",
        "date": "2016-04-07",
        "locked": true,
        "field": "steps",
        "winners": [
            {
                "name": "Demo User",
                "email": "person@demo.com",
                "guid": "1234",
                "picture": "https://www.pic.com/img.png",
                "strap": { ... }
            }
        ],
        "data": [
            {
                "guid": "1234",
                "activeMinutes": 370,
                "calories": 4018,
                "floors": 32,
                "nonactiveMinutes": 960,
                "distance": 16.49,
                "steps": 21147,
                "updated": "April 7th 2016, 10:10:25 pm",
                "name": "Demo User",
                "email": "person@demo.com",
                "guid": "1234",
                "picture": "https://www.pic.com/img.png",
                "strap": { ... }
            }, { ... }
        ]
    }, { ... }
]
```
<br>
*Challenge's Leaderboards Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/leaderboard/test_daily"
```
<br>
*Challenge's Leaderboards Response*
```json
[
    {
        "slug": "test_daily",
        "period": "daily",
        "date": "2016-04-07",
        "locked": true,
        "field": "steps",
        "winners": [
            {
                "name": "Demo User",
                "email": "person@demo.com",
                "guid": "1234",
                "picture": "https://www.pic.com/img.png",
                "strap": { ... }
            }
        ],
        "data": [
            {
                "guid": "1234",
                "activeMinutes": 370,
                "calories": 4018,
                "floors": 32,
                "nonactiveMinutes": 960,
                "distance": 16.49,
                "steps": 21147,
                "updated": "April 7th 2016, 10:10:25 pm",
                "name": "Demo User",
                "email": "person@demo.com",
                "guid": "1234",
                "picture": "https://www.pic.com/img.png",
                "strap": { ... }
            }, { ... }
        ]
    }, { ... }
]
```
<br>
*Single Challenge's Leaderboard by Date Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/leaderboard/test_daily/2016-04-07"
```
<br>
*All Users Response*
```json
{
    "slug": "test_daily",
    "period": "daily",
    "date": "2016-04-07",
    "locked": true,
    "field": "steps",
    "winners": [
        {
            "name": "Demo User",
            "email": "person@demo.com",
            "guid": "1234",
            "picture": "https://www.pic.com/img.png",
            "strap": { ... }
        }
    ],
    "data": [
        {
            "guid": "1234",
            "activeMinutes": 370,
            "calories": 4018,
            "floors": 32,
            "nonactiveMinutes": 960,
            "distance": 16.49,
            "steps": 21147,
            "updated": "April 7th 2016, 10:10:25 pm",
            "name": "Demo User",
            "email": "person@demo.com",
            "guid": "1234",
            "picture": "https://www.pic.com/img.png",
            "strap": { ... }
        }, { ... }
    ]
}
```