---
id: jest-with-playwright
title: Run your Jest test scripts with Playwright on LambdaTest
hide_title: true
sidebar_label: Jest
description: Run your Jest scripts with Playwright on LambdaTest scalable cloud grid of 50+ real desktop browsers and operating systems.
keywords:
  - jest playwright
  - jest automation testing
  - playwrightjest 
  - playwright jest testing guide
  - jest playwright framework

url: https://www.lambdatest.com/support/docs/jest-with-playwright/
site_name: LambdaTest
slug: jest-with-playwright/
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
          "name": "Jest with Playwright",
          "item": "https://www.lambdatest.com/support/docs/jest-with-playwright/"
        }]
      })
    }}
></script>

# Jest with Playwright: Running Your First Test
* * *

Learn how to use Playwright with Jest framework to automate web application testing across 50+ real browsers and operating systems on LambdaTest cloud platform.

## Prerequisites
***

>Note: All the code samples in this documentation can be found in the LambdaTest's Repository on GitHub. You can either download or clone the repository to quickly run your tests.
<a href="https://github.com/LambdaTest/playwright-sample/tree/main/playwright-test-js" className="github__anchor"><img loading="lazy" src={require('../assets/images/icons/github.png').default} alt="Image"  className="doc_img"/> View on GitHub</a>

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

4. To run Playwright tests, set your LambdaTest Username and Access key in the Environment Variables.


## Run your Playwright tests with Jest
---

Navigate to the `jest-playwright.config.js` file in the `playwright-jest-js` directory and provide your LambdaTest Username and Access key.

```js
const cp = require('child_process');
const playwrightClientVersion = cp.execSync('npx playwright --version').toString().trim().split(' ')[1];

const caps_chromium = {
  'browserName': 'pw-chromium', // Browsers allowed: `Chrome`, `MicrosoftEdge`, `pw-chromium`, `pw-firefox` and `pw-webkit`
  'browserVersion': 'latest',
  'LT:Options': {
    'platform': 'Windows 10',
    'build': 'Playwright-Jest Build',
    'name': 'Playwright-Jest Test on Chromium',
    'user': process.env.LT_USERNAME,
    'accessKey': process.env.LT_ACCESS_KEY,
    'network': true,
    'video': true,
    'console': true,
    'tunnel': false, // Add tunnel configuration if testing locally hosted webpage
    'tunnelName': '', // Optional
    'geoLocation': '', // country code can be fetched from https://www.lambdatest.com/capabilities-generator/
    'playwrightClientVersion': playwrightClientVersion
  }
};

const caps_firefox = {
  'browserName': 'pw-firefox', // Browsers allowed: `Chrome`, `MicrosoftEdge`, `pw-chromium`, `pw-firefox` and `pw-webkit`
  'browserVersion': 'latest',
  'LT:Options': {
    'platform': 'Windows 10',
    'build': 'Playwright-Jest Build ',
    'name': 'Playwright-Jest Test on Firefox',
    'user': process.env.LT_USERNAME,
    'accessKey': process.env.LT_ACCESS_KEY,
    'network': true,
    'video': true,
    'console': true,
    'tunnel': false, // Add tunnel configuration if testing locally hosted webpage
    'tunnelName': '', // Optional
    'geoLocation': '', // country code can be fetched from https://www.lambdatest.com/capabilities-generator/
  }
};

const caps_webkit = {
  'browserName': 'pw-webkit', // Browsers allowed: `Chrome`, `MicrosoftEdge`, `pw-chromium`, `pw-firefox` and `pw-webkit`
  'browserVersion': 'latest',
  'LT:Options': {
    'platform': 'Windows 10',
    'build': 'Playwright-Jest Build',
    'name': 'Playwright-Jest Test on WebKit',
    'user': process.env.LT_USERNAME,
    'accessKey': process.env.LT_ACCESS_KEY,
    'network': true,
    'video': true,
    'console': true,
    'tunnel': false, // Add tunnel configuration if testing locally hosted webpage
    'tunnelName': '', // Optional
    'geoLocation': '', // country code can be fetched from https://www.lambdatest.com/capabilities-generator/
  }
};

module.exports = {
    connectOptions: {
        chromium: {
          wsEndpoint: `wss://cdp.lambdatest.com/playwright?capabilities=${encodeURIComponent(JSON.stringify(caps_chromium))}`
        },
        firefox: {
          wsEndpoint: `wss://cdp.lambdatest.com/playwright?capabilities=${encodeURIComponent(JSON.stringify(caps_firefox))}`
        },
        webkit: {
            wsEndpoint: `wss://cdp.lambdatest.com/playwright?capabilities=${encodeURIComponent(JSON.stringify(caps_webkit))}`
        }
      },
      browsers: ['chromium', 'firefox', 'webkit'],
}
```

Pass the below command in the terminal to run the test.

```js
npm run test
```

## View your test results
---

Go to the [LambdaTest Automation dashboard](https://automation.lambdatest.com/build) to see your Playwright JavaScript test results.




