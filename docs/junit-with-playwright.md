---
id: junit-with-playwright
title: Run your JUnit automation scripts with Playwright on LambdaTest
hide_title: true
sidebar_label: JUnit
description: Run your JUnit automation scripts with Playwright on LambdaTest scalable cloud grid of 50+ real desktop browsers and operating systems.
keywords:
  - junit playwright
  - junit automation testing
  - playwright junit
  - playwright junit testing guide
  - junit playwright framework

url: https://www.lambdatest.com/support/docs/junit-with-playwright/
site_name: LambdaTest
slug: junit-with-playwright/
---

import CodeBlock from '@theme/CodeBlock';
import {YOUR_LAMBDATEST_USERNAME, YOUR_LAMBDATEST_ACCESS_KEY} from "@site/src/component/keys";

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
          "name": "JUnit with Playwright",
          "item": "https://www.lambdatest.com/support/docs/junit-with-playwright/"
        }]
      })
    }}
></script>

# JUnit with Playwright: Running Your First Test
* * *

Learn how to use Playwright with JUnit to automate web application testing across 50+ real browsers and operating systems on LambdaTest cloud platform.


## Prerequisites
***

>Note: All the code samples in this documentation can be found in the LambdaTest's Repository on GitHub. You can either download or clone the repository to quickly run your tests.
<a href="https://github.com/LambdaTest/playwright-sample/tree/main/playwright-java-junit" className="github__anchor"><img loading="lazy" src={require('../assets/images/icons/github.png').default} alt="Image"  className="doc_img"/> View on GitHub</a>

1. Clone the LambdaTest-Playwright repository on your system.

```js
git clone https://github.com/LambdaTest/playwright-sample.git
cd playwright-sample-main
```

2. Install the npm dependencies.

```
npm install
```

3. A LambdaTest Username and Access key. You can get it from your LambdaTest Profile section. Don't have an account, [sign up for free](https://accounts.lambdatest.com/register).

<img loading="lazy" src={require('../assets/images/playwright-testing/key.webp').default} alt="Image" width="1444" height="703"  className="doc_img"/>

## Run your Playwright tests with JUnit
---

Navigate to the `LTCapability.JUnit` file and provide your LambdaTest Username and Access key.

```java
import com.google.gson.JsonObject;
import com.tngtech.JUnit.junit.dataprovider.DataProvider;

public class LTCapability {
  @DataProvider
  public static Object[] getDefaultTestCapability() {
    JsonObject capabilities1 = new JsonObject();
    JsonObject ltOptions1 = new JsonObject();

    String user = System.getenv("LT_USERNAME");
    String accessKey = System.getenv("LT_ACCESS_KEY");

    capabilities1.addProperty("browserName", "Chrome"); // Browsers allowed: `Chrome`, `MicrosoftEdge`, `pw-chromium`, `pw-firefox` and `pw-webkit`
    capabilities1.addProperty("browserVersion", "latest");
    ltOptions1.addProperty("platform", "Windows 10");
    ltOptions1.addProperty("name", "Playwright Test");
    ltOptions1.addProperty("build", "Playwright Testing using Junit");
    ltOptions1.addProperty("user", user);
    ltOptions1.addProperty("accessKey", accessKey);
    capabilities1.add("LT:Options", ltOptions1);


    JsonObject capabilities2 = new JsonObject();
    JsonObject ltOptions2 = new JsonObject();
    capabilities2.addProperty("browserName", "MicrosoftEdge"); // Browsers allowed: `Chrome`, `MicrosoftEdge`, `pw-chromium`, `pw-firefox` and `pw-webkit`
    capabilities2.addProperty("browserVersion", "latest");
    ltOptions2.addProperty("platform", "Windows 10");
    ltOptions2.addProperty("name", "Playwright Test");
    ltOptions2.addProperty("build", "Playwright Testing using Junit");
    ltOptions2.addProperty("user", user);
    ltOptions2.addProperty("accessKey", accessKey);
    capabilities2.add("LT:Options", ltOptions2);
    return new Object[]{
      capabilities1,capabilities2
    };
  }
}
```

Pass the below command in the terminal to run the test.

```java
mvn -Dexec.mainClass="com.lambdatest.LTCapability" -Dexec.classpathScope=test test-compile exec:java
```

## View your test results
---

Go to the [LambdaTest Automation dashboard](https://automation.lambdatest.com/build) to see your Playwright JUnit test results.




