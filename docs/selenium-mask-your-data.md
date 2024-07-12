---
id: selenium-mask-your-data
title: Mask your Sensitive Data
hide_title: false
sidebar_label: Masking Sensitive Data
description: This capability allows you to mask your sensitive data such as username and acceskey while showing in the logs of the lambdatest platform
keywords:
  - lambdatest automation
  - selenium automation grid
  - selenium masking data
  - lambda mask commands
url: https://www.lambdatest.com/support/docs/selenium-mask-your-data/
site_name: LambdaTest
slug: selenium-mask-your-data/
---

<script type="application/ld+json"
      dangerouslySetInnerHTML={{ __html: JSON.stringify({
       "@context": "https://schema.org",
        "@type": "BreadcrumbList",
        "itemListElement": [{
          "@type": "ListItem",
          "position": 1,
          "name": "LambdaTest",
          "item": "https://www.lambdatest.com"
        },{
          "@type": "ListItem",
          "position": 2,
          "name": "Other Capabilities",
          "item": "https://www.lambdatest.com/support/docs/"
        },{
          "@type": "ListItem",
          "position": 3,
          "name": "Mask your Data",
          "item": "https://www.lambdatest.com/support/docs/selenium-mask-your-data/"
        }]
      })
    }}
></script>

With the help of **maskCommands** capability, you can now hide sensitive and important data, sent to or retrieve from the remote browsers at LambdaTest. When used, this will hide all the keystrokes and other required values, and replace them with **‘*’** in test session logs (both text and raw).

**Syntax (Java)**:

`capabilities.setCapability("lambdaMaskCommands", {"<array of values to be hidden>"});`

List of comma separated values that can be hidden:

| Value | Description |
|-------|-------------|
| `setValues`	| Hide/Redact all the text sent via sendKeys command. |
| `setCookies` | Hide/Redact all the cookies set by the addCookie command.|
| `getCookies` | Hide/Redact all the cookie values obtained using the getCookies and getCookieNamed command.|

For example:

| Language | Example |
|-------|-------------|
| Java	|`capabilities.setCapability(“lambdaMaskCommands”, &lbrace;“setValues”, “setCookies, getCookies”&rbrace;);` |
| Node.js | `capabilities[‘lambdaMaskCommands’] = [“setValues”, “setCookies”, “getCookies”]`|
| C# | `capabilities.SetCapability(“lambdaMaskCommands”, &lbrace;“setValues”, “setCookies”, “getCookies”&rbrace;);`|
| PHP	| `$capabilities[“lambdaMaskCommands”] = array(“setValues”, “setCookies”, “getCookies”)`|
| Python | `capabilities[“lambdaMaskCommands”] = [“setValues”, “setCookies”, “getCookies”]`|
| Ruby |`capabilities[“lambdaMaskCommands”] = [“setValues”, “setCookies”, “getCookies”]`|