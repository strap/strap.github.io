---
title: "Authentication"
excerpt: ""
---
To retrieve reports from the Report API, you must pass a valid read token to any of our available API endpoints. To do this, set an HTTP header for x-auth-token equal to your read token. Because your project is associated with your read token, any project level API calls will use the token to determine the project id.
[block:code]
{
  "codes": [
    {
      "code": "$ curl \"https://api2.straphq.com/users\" --header \"x-auth-token: abc123xyz\"",
      "language": "curl",
      "name": "Example API call passing read token\n"
    }
  ]
}
[/block]