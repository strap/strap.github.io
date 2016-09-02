---
title: "Challenges"
excerpt: ""
---
### GET /api/challenge/{slug}
The challenge route will return the list of challenges or a single challenge if the optional **slug** parameter is defined.

*All Challenges Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/challenge"
```
<br>
*All Challenges Response*
```json
[
    {
        "title": "Test Daily",
        "slug": "test_daily",
        "description": "Description about a really sweet challenge",
        "details": {
            "overview": "Challenge Description",
            "field": "steps",
            "selection": "top",
            "number": "1",
            "period": "daily",
            "open": "2016-04-04",
            "start": "2016-04-06",
            "end": "2016-05-01"
        },
        "prize": {
            "title": "Demo Prize",
            "icon": "https://www.prize.com/img.png",
            "description": "Prize Description",
            "url": ""
        },
        "theme": {
            "bg": "https://www.theme.com/img.png",
            "primary": "#ff6e00",
            "secondary": "#ffffff",
            "pallet": "dark"
        },
        "terms": "Optional Challenge specific terms",
        "privacy": "Optional Challenge specific privacy policy",
        "users": [
            {
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
*Single Challenge Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/challenge/test_daily"
```
<br>
*Single Challenge Response*
```json
{
    "title": "Test Daily",
    "slug": "test_daily",
    "description": "Description about a really sweet challenge",
    "details": {
        "overview": "Challenge Description",
        "field": "steps",
        "selection": "top",
        "number": "1",
        "period": "daily",
        "open": "2016-04-04",
        "start": "2016-04-06",
        "end": "2016-05-01"
    },
    "prize": {
        "title": "Demo Prize",
        "icon": "https://www.prize.com/img.png",
        "description": "Prize Description",
        "url": ""
    },
    "theme": {
        "bg": "https://www.theme.com/img.png",
        "primary": "#ff6e00",
        "secondary": "#ffffff",
        "pallet": "dark"
    },
    "terms": "Optional Challenge specific terms",
    "privacy": "Optional Challenge specific privacy policy",
    "users": [
        {
            "name": "Demo User",
            "email": "person@demo.com",
            "guid": "1234",
            "picture": "https://www.pic.com/img.png",
            "strap": { ... }
        }, { ... }
    ]
}
```