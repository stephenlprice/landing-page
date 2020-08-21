![API Guild](https://github.com/stephenlprice/landing-page/blob/main/assets/images/logos/apiguild.png?raw=true)
![API Guild](https://github.com/stephenlprice/landing-page/blob/main/assets/images/collaboration/design-collab.png?raw=true)

#### With this workspace, you can: 

- Share interactive documentation with internal and external stakeholders
- Explore your APIs, track dependencies and view changelogs
- Invite team members to collaborate on API assets
- Create and update API designs and documentation
***

## Getting Started

Dig into the [documentation and quickstarts](https://meta.stoplight.io) to govern, design, and document APIs. The workspace has you covered with everything from an interactive API explorer, automatic mock servers, OpenAPI designer, API console, code samples in your favorite languages, and comprehensive examples.

<!-- theme: warning -->

>If you are a member of this workspace, please log in [here](auth) 🔐.
>
>Don't forget to [invite team members](admin/members) to collaborate on API designs.

***

## 🔎 Discovery

Use the `Explorer` funcionality to [find APIs](explore), try out hosted ***mock servers***, track ***dependencies***, view ***changelogs*** and star your favorite artifacts.

![explorer](https://github.com/stephenlprice/landing-page/blob/main/assets/images/product/explorer.gif?raw=true)

<!-- theme: info -->

>💡 [Add projects](add/projects) into the workspace so that others can find and ***USE*** your APIs. Never again will someone build an endpoint to replace your hardwork!

***

## 🛠 Design

Help architects design beautiful APIs quickly. Use `Studio` to write actionable ***API descriptions*** that can power your development workflow. Enjoy the benefits of a ***split-stack development***, up-to-date documentation and the developer experience you deserve!

![studio](https://github.com/stephenlprice/landing-page/blob/main/assets/images/product/studio.png?raw=true)

<!-- theme: info -->

>Connect Git repos to collaborate on OpenAPI descriptions, JSON Schemas, and markdown articles into your workspace or publish your local files via CLI by [clicking here](add/projects). 🚀

***

## 📖 Documentation

Provide an amazing developer experience for internal and external developers. Keep your documentation up to date with built-in git webhooks or add the CLI to your CI pipelines. Support multiple versions of documentation with branches.

![studio](https://github.com/stephenlprice/landing-page/blob/main/assets/images/product/studio.png?raw=true)

### Code Generation

Client-side code generation is provided by the API documentation automatically. Here is an example:

```javascript
var data = null;

var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    console.log(this.responseText);
  }
});

xhr.open("GET", "https://cloudhome.io/api/devices/123?spaceid=all&sort=desc&limit=10");
xhr.setRequestHeader("deviceid", "all");
xhr.setRequestHeader("apikey", "123");

xhr.send(data);
```

### Interactive Documentation

With the `'Try It!'` functionality you can send requests directly to API servers or you can use the built-in mock server. Click `'Send'` in the embedded _**Request Maker**_ below to get a sample mocked response:

```json http
{
  "method": "get",
  "url": "https://apiguild.stoplight.io/mocks/apiguild/cloudhome/30785/api/devices/abc",
  "query": {
    "spaceid": "all",
    "sort": "desc",
    "limit": "10"
  },
  "headers": {
    "deviceid": "all",
    "apiKey": "123",
    "Prefer": "code=200, example=devices"
  }
}
```

### Data Models

This workspace is also a great place to design and display schemas:
</br>

```json json_schema
{
  "title": "Device",
  "type": "object",
  "x-tags": [
    "devices",
    "IOT"
  ],
  "description": "Describes a device activated on a **CloudHome** account. Each class can contain more than one device and location, centrally managed by the CloudHome service cloud.",
  "x-examples": {
    "devices": [
      {
        "deviceID": "123",
        "deviceName": "frontDoorLock",
        "deviceClass": "safety",
        "spaceID": "home",
        "alexaCompatible": true,
        "storageUsed": 0.003,
        "storageFree": 1
      },
      {
        "deviceID": "456",
        "deviceName": "thermostat",
        "deviceClass": "comfort",
        "spaceID": "home",
        "alexaCompatible": true,
        "storageUsed": 0.025,
        "storageFree": 1
      },
      {
        "deviceID": "789",
        "deviceName": "sprinkler",
        "deviceClass": "convenience",
        "spaceID": "yard",
        "alexaCompatible": false,
        "storageUsed": 0.0018,
        "storageFree": 1
      }
    ],
    "device": [
      {
        "deviceID": "abc",
        "deviceName": "welcomeDroid",
        "deviceClass": "commercial",
        "spaceID": "office",
        "alexaCompatible": true,
        "storageUsed": 137,
        "storageFree": 300
      }
    ]
  },
  "properties": {
    "deviceID": {
      "type": "string",
      "description": "generated by the backend"
    },
    "deviceName": {
      "type": "string",
      "description": "user generated name"
    },
    "deviceClass": {
      "type": "string"
    },
    "spaceID": {
      "type": "string"
    },
    "alexaCompatible": {
      "type": "boolean"
    },
    "storageUsed": {
      "type": "number",
      "description": "in gigabytes as described in this [data measurement chart](http://www.wu.ece.ufl.edu/links/dataRate/DataMeasurementChart.html)\n"
    },
    "storageFree": {
      "type": "number",
      "description": "in gigabytes as described in this [data measurement chart](http://www.wu.ece.ufl.edu/links/dataRate/DataMeasurementChart.html)"
    },
    "dateCreated": {
      "type": "string",
      "format": "date-time",
      "example": "2017-07-21T17:32:28Z",
      "pattern": "/^(?<fullyear>\\d{4})-(?<month>0[1-9]|1[0-2])-(?<mday>0[1-9]|[12][0-9]|3[01])T(?<hour>[01][0-9]|2[0-3]):(?<minute>[0-5][0-9]):(?<second>[0-5][0-9]|60)(?<secfrac>\\.[0-9]+)?(Z|(\\+|-)(?<offset_hour>[01][0-9]|2[0-3]):(?<offset_minute>[0-5][0-9]))$/i"
    },
    "dateUpdated": {
      "type": "string",
      "format": "date-time",
      "pattern": "/^(?<fullyear>\\d{4})-(?<month>0[1-9]|1[0-2])-(?<mday>0[1-9]|[12][0-9]|3[01])T(?<hour>[01][0-9]|2[0-3]):(?<minute>[0-5][0-9]):(?<second>[0-5][0-9]|60)(?<secfrac>\\.[0-9]+)?(Z|(\\+|-)(?<offset_hour>[01][0-9]|2[0-3]):(?<offset_minute>[0-5][0-9]))$/i",
      "example": "2017-07-21T17:32:28Z"
    }
  },
  "required": [
    "deviceName"
  ]
}
```

***

## Liked what you saw?

Get in touch and let us know how we can help.

<!--
type: tab
title: 🦸🏼‍♀️ Contact Sales
-->

Contact sales at [sales@stoplight.io](mailto:sales@stoplight.io) to get help from our team of in-house experts.

<!--
type: tab
title: 🧙🏼‍♂️ Contact Support
-->

Contact Support at [support@stoplight.io](mailto:support@stoplight.io) for help with your hardest technical questions.


<!--
type: tab
title: 👋 Ask the Community
-->

Ask a peer in our community forum about how they use the Stoplight Platform.

[Go to Community](https://community.stoplight.io)

<!-- type: tab-end -->

Built with ❤️ by [Stoplight](https://stoplight.io). Public icons by [Icons S8](https://icons8.com). Created my free logo at [LogoMakr.com](https://logomakr.com/). Images from [Unsplash.com](https://unsplash.com/).