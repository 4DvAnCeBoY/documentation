---
id: regular-expression-xcui
title: Regular Expression - XCUI
# hide_title: true
sidebar_label: Regular Expression
description: There may be instances when the device you chose for a test on LambdaTest is not available. In these scenarios, REGEX will help you widen the search request for devices to run the test on.
keywords:
- regular expression lambdatest
- regular expression app automation
url: https://www.lambdatest.com/support/docs/regular-expression-xcui/
site_name: LambdaTest
slug: regular-expression-xcui/
---

<script type="application/ld+json"
      dangerouslySetInnerHTML={{ __html: JSON.stringify({
       "@context": "https://schema.org",
        "@type": "BreadcrumbList",
        "itemListElement": [{
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://www.lambdatest.com"
        },{
          "@type": "ListItem",
          "position": 2,
          "name": "Support",
          "item": "https://www.lambdatest.com/support/docs/"
        },{
          "@type": "ListItem",
          "position": 3,
          "name": "App Automation: Regular Expression",
          "item": "https://www.lambdatest.com/support/docs/regular-expression-xcui/"
        }]
      })
    }}
></script>
Regular Expression or REGEX is widely used to make searching/find characters in a string.

When you run a test on LambdaTest using a specific device, there may be scenarios, in which the particular device that you selected isn’t available. In these scenarios, REGEX will help you widen the search request for devices to run the test on.

To quote an example, consider you want to run the test on an iPhone. It doesn’t matter which one, but it’s got to be an iPhone. In these cases, we can use REGEX to specify exactly that. You’ll now be allotted any iPhone that’s available which widens the search of devices considerably.

Platform version is not mandatory only if `deviceName` is passed using regex. If there is no regex in `deviceName`, passing `platformVersion` is mandatory.

Usual way to pass the `deviceName` and `platformVersion` looks like this: <br/>

```java
"device" : ["Pixel 6 Pro-12"]
```

Passing `deviceName` using REGEX:<br/>
```java
"device" : ["Pixel.*-12"]
```

:::tip Right way to pass REGEX:

``Pixel.*-12`` <br/>
``Pixel.*``

:::

:::caution
REGEX is currently possible on the `deviceName` as of now and *not* on the ``platformVerison``. <br/>
:::