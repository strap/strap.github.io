---
title: "Users"
excerpt: ""
---
### GET /api/user/{guid}
The user route will return the list of users or a single user if the optional **guid** parameter is defined.  If retrieving all users, you may filter on the user join date.

*All Users Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/user"
```
<br>
*All Users Response*
```json
[
    {
        "name": "Demo User",
        "email": "person@demo.com",
        "guid": "1234",
        "picture": "https://www.pic.com/img.png",
        "createdAt": "2016-06-20T18:57:34.841Z",
        "strap": { ... }
    },
    { ... }
]
```

*All Users Who Joined On Date Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/user?date=2016-06-20"
```
<br>
*All Users Who Joined On Date Response*
```json
[
    {
        "name": "Demo User",
        "email": "person@demo.com",
        "guid": "1234",
        "picture": "https://www.pic.com/img.png",
        "createdAt": "2016-06-20T18:57:34.841Z",
        "strap": { ... }
    },
    { ... }
]
```
<br>
*All Users Who Joined In Range Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/user?start=2016-06-19&end=2016-06-21"
```
<br>
*All Users Who Joined In Range Response*
```json
[
    {
        "name": "Demo User",
        "email": "person@demo.com",
        "guid": "1234",
        "picture": "https://www.pic.com/img.png",
        "createdAt": "2016-06-20T18:57:34.841Z",
        "strap": { ... }
    },
    { ... }
]
```
<br>
*All Users Who Have Joined Since Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/user?start=2016-06-20T18:00:00.000Z"
```
<br>
*All Users Who Joined In Range Response*
```json
[
    {
        "name": "Demo User",
        "email": "person@demo.com",
        "guid": "1234",
        "picture": "https://www.pic.com/img.png",
        "createdAt": "2016-06-20T18:57:34.841Z",
        "strap": { ... }
    },
    { ... }
]
```
<br>
*Single User Request*
```
$ curl –H "x-token: "%%%TOKEN%%%" "https://%%%HOST%%%/api/user/1234"
```
<br>
*Single User Response*
```json
{
    "name": "Demo User",
    "email": "person@demo.com",
    "guid": "1234",
    "picture": "https://www.pic.com/img.png",
    "createdAt": "2016-06-20T18:57:34.841Z",
    "strap": { ... }
}
```
<a name="challenge"></a>
<hr></hr>


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