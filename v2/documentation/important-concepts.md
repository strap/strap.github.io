---
title: "Important Concepts"
excerpt: ""
---
Your journey to getting started will look different depending on whether you're using **Strap Integrate** or **Strap Engage**.

If you are building a mobile app or web app and want to enable users to connect their devices and health apps, you'll want to use the Strap Integrate SDK.

If you'd rather not develop a custom solution that leverages fitness and health data, Strap Engage is a lightweight option for getting users connected very quickly. Engage features customizable fitness and activity challenges. 
[block:callout]
{
  "type": "info",
  "body": "Whether you're using Strap Integrate or Strap Engage, access to normalized, aggregated health and fitness data takes place via the Report API.",
  "title": "Important!"
}
[/block]

## The GUID ##

Every human who connects his or her device to your app is identified by a globally unique identifier, or **guid**. 

When using Strap Integrate, you'll generate and keep track of a **guid** representing a user. The **guid** is used when calling our API endpoints, and when calling functions for connecting users in the SDK. 

In Strap Engage, the **guid** is generated automatically. To retrieve user data for users created by Engage, you'll make API calls to the Engage API to find a relevant **guid**, then use the guid(s) in calls to the Report API.

## Access Tokens ##

Every Strap project has a Read Token and a Write Token, which are accessible via the Strap Console or through your account manager. These tokens should be kept safe and treated like a password (especially your write token).