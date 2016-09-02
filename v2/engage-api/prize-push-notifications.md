---
title: "Prize Push Notifications"
excerpt: ""
---
If you elect to receive push notifications on awarded challenge prizes, a POST will be issued to your provided url.  The POST body will be of the following format.

```json
{  
    "challenge":{  
        "title":"Challenge name",
        "slug":"Challenge slug",
        "period":"daily",
        "field":"steps",
        "date":"2016-06-01"
    },
    "winners":[  
        {  
            "name":"Winner Name",
            "email":"winner@email.com",
            "guid":"winner-guid",
            "value":3762
        }
    ]
}
```