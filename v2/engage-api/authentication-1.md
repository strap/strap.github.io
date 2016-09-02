---
title: "Authentication"
excerpt: ""
---
Each Engage API instance is sandboxed and siloed per customer. Before you can make calls the Engage API, your Strap account rep will provide you with a URL and Token for Engage API access. 

Once you have an Engage API URL and Token, simply set set an HTTP header for x-token equal to your Engage API token. 


[block:code]
{
  "codes": [
    {
      "code": "$ curl –H \"x-token: \"f93ce1328e44b821d92bcbb2c47362e9\" \"https://engage-instance-url/api/user\"",
      "language": "curl",
      "name": "Sample Engage API Call"
    }
  ]
}
[/block]