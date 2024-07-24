---
id: javascript-with-playwright
title: Run your JavaScript automation scripts with Playwright on LambdaTest
hide_title: true
sidebar_label: JavaScript
description: Run your JavaScript automation scripts with Playwright on LambdaTest scalable cloud grid of 50+ real desktop browsers and operating systems.
keywords:
  - javascript playwright
  - javascript automation testing
  - playwright javascript
  - playwright javascript testing guide
  - javascript playwright framework

url: https://www.lambdatest.com/support/docs/javascript-with-playwright/
site_name: LambdaTest
slug: javascript-with-playwright/
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
          "name": "JavaScript with Playwright",
          "item": "https://www.lambdatest.com/support/docs/javascript-with-playwright/"
        }]
      })
    }}
></script>

# JavaScript with Playwright: Running Your First Test
* * *

Learn how to use Playwright with JavaScript to automate web application testing across 50+ real browsers and operating systems on LambdaTest cloud platform.


## Prerequisites
***

>Note: All the code samples in this documentation can be found in the LambdaTest's Repository on GitHub. You can either download or clone the repository to quickly run your tests.
<a href="https://github.com/LambdaTest/playwright-sample/tree/main/playwright-test-js" className="github__anchor"><img loading="lazy" src={require('../assets/images/icons/github.png').default} alt="Image"  className="doc_img"/> View on GitHub</a>

1. Clone the LambdaTest-Playwright repository on your system.

```js
git clone https://github.com/LambdaTest/playwright-sample.git
cd playwright-sample
cd playwright-test-js
```

2. Install the npm dependencies.

```
npm install
```

3. A LambdaTest Username and Access key. You can get it from your LambdaTest Profile section. Don't have an account, [sign up for free](https://accounts.lambdatest.com/register).

<img loading="lazy" src={require('../assets/images/legacy_platform_to_lambdatest/auth.png').default} alt="Image" width="1444" height="703"  className="doc_img"/>

4. To run Playwright tests, set your LambdaTest Username and Access key in the Environment Variables.

## Run your Playwright tests with JavaScript
---

Navigate to the `lambdatest-setup.js` file in the `playwright-test-js` directory.

```js
/**
 * Add the file in your test suite to run tests on LambdaTest.
 * Import `test` object from this file in the tests.
 */
const base = require('@playwright/test')
const path = require('path')
const { chromium } = require('playwright')
const cp = require('child_process');
const playwrightClientVersion = cp.execSync('npx playwright --version').toString().trim().split(' ')[1];

// LambdaTest capabilities
const capabilities = {
  'browserName': 'Chrome', // Browsers allowed: `Chrome`, `MicrosoftEdge`, `pw-chromium`, `pw-firefox` and `pw-webkit`
  'browserVersion': 'latest',
  'LT:Options': {
    'platform': 'Windows 10',
    'build': 'Playwright Build',
    'name': 'Playwright Test',
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
}

// Patching the capabilities dynamically according to the project name.
const modifyCapabilities = (configName, testName) => {
  let config = configName.split('@lambdatest')[0]
  let [browserName, browserVersion, platform] = config.split(':')
  capabilities.browserName = browserName ? browserName : capabilities.browserName
  capabilities.browserVersion = browserVersion ? browserVersion : capabilities.browserVersion
  capabilities['LT:Options']['platform'] = platform ? platform : capabilities['LT:Options']['platform']
  capabilities['LT:Options']['name'] = testName
}

const getErrorMessage = (obj, keys) => keys.reduce((obj, key) => (typeof obj == 'object' ? obj[key] : undefined), obj)

exports.test = base.test.extend({
  page: async ({ page, playwright }, use, testInfo) => {
    // Configure LambdaTest platform for cross-browser testing
    let fileName = testInfo.file.split(path.sep).pop()
    if (testInfo.project.name.match(/lambdatest/)) {
      modifyCapabilities(testInfo.project.name, `${testInfo.title} - ${fileName}`)

      const browser = await chromium.connect({
        wsEndpoint: `wss://cdp.lambdatest.com/playwright?capabilities=${encodeURIComponent(JSON.stringify(capabilities))}`
      })

      const ltPage = await browser.newPage(testInfo.project.use)
      await use(ltPage)

      const testStatus = {
        action: 'setTestStatus',
        arguments: {
          status: testInfo.status,
          remark: getErrorMessage(testInfo, ['error', 'message'])
        }
      }
      await ltPage.evaluate(() => {},
        `lambdatest_action: ${JSON.stringify(testStatus)}`)
      await ltPage.close()
      await browser.close()
    } else {
      // Run tests in local in case of local config provided
      await use(page)
    }
  }
})
```

Pass the below command in the terminal to run the test.

```js
npm run test
```

## View your test results
---

Go to the [LambdaTest Automation dashboard](https://automation.lambdatest.com/build) to see your Playwright JavaScript test results.




