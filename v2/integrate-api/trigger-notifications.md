---
title: "Trigger Notifications"
excerpt: ""
---
Triggers are setup in the Strap Console for your project.  Each trigger is assigned a set of criteria that will be evaluated against the information coming into the Strap system for each user.

Notifications provide the ability for your application to receive real-time push alerts that a user or set of users have met the criteria of your triggers.

The Trigger notification is delivered as a JSON-based POST from our servers to the Notification URL specified for each trigger.  The Notification URL should respond immediately with a 200 and process the trigger  POST information following the 200 response.

## Example Notification POST

```POST``` **https://example.com/triggers**

#### POST Body
```
{
    "trigger": "key-of-trigger", // Trigger Key
    "triggerID": "qwesdf23f",    // Strap Trigger ID
    "projectId": "wewfesdqwer",  // Strap Project ID
    "users": [{
            "guid": "qwersd-wddfadfasd", // User GUID
            "report": "r78urtjhbsef", // Report ID
            "url": "https://api2.straphq.com/report/r78urtjhbsef", // API URL
            "meta": {
                "conditions": [
                  {
                    "comparison": ">",
                    "description": "User's steps (2501.0) is  greater than 2500 for the day of 2016-02-25",
                    "field": "steps",
                    "percent": false,
                    "section": "activity",
                    "threshold": 2500,
                    "value": 2501
                  }
                ],
                "range": "day",
                "type": "aggregate"
            }
          }
        }, {
            "guid": "ryujh-65798itrhgsd", // User GUID
            "report": "sfgsfgsertwert", // Report ID
            "url": "https://api2.straphq.com/report/sfgsfgsertwert", // API URL
            "meta": {
                "conditions": [
                  {
                    "comparison": ">",
                    "description": "User's steps (2501.0) is  greater than 2500 for the day of 2016-02-25",
                    "field": "steps",
                    "percent": false,
                    "section": "activity",
                    "threshold": 2500,
                    "value": 2501
                  }
                ],
                "range": "day",
                "type": "aggregate"
            }
        }]
}

```