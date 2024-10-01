---
id: selenium-bidi-integration
title: BiDi Testing with Selenium WebDriver on LambdaTest
hide_title: false
sidebar_label: BiDi Testing
description: Discover BiDi testing with Selenium WebDriver on LambdaTest. Enjoy enhanced automation, seamless cross-browser support, fine-grained control, and future-proof your test suite
keywords:
  - lambdatest automation
  - selenium automation grid
  - selenium bidi testing
  - online selenium automation
url: https://www.lambdatest.com/support/docs/selenium-bidi-integration/
site_name: LambdaTest
slug: selenium-bidi-integration/
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
          "name": "Knowledge Base",
          "item": "https://www.lambdatest.com/support/docs/"
        },{
          "@type": "ListItem",
          "position": 3,
          "name": "Selenium BiDi Testing",
          "item": "https://www.lambdatest.com/support/docs/selenium-bidi-integration/"
        }]
      })
    }}
></script>
Selenium WebDriver BiDi is a W3C standard protocol used to establish communication between a test script and a remote WebDriver server. It introduces bi-directional communication, which means both the script and the browser can send requests and responses, leading to a more dynamic and reactive testing experience.

> BiDi is compatible with **Chrome**, **Firefox**, and **Edge** browsers. For more information, please refer to the [documentation](https://wpt.fyi/results/webdriver/tests/bidi?label=stable&label=master&aligned).

## Why to use WebDriver BiDi Protocol?

There are several compelling reasons to consider using BiDi testing with Selenium WebDriver on LambdaTest:

- **Enhanced Test Maintainability :** Traditional WebDriver relies on a request-response model, where the test script dictates every action. BiDi introduces a standardized protocol, making your tests less vulnerable to breaking due to browser version changes. This reduces maintenance overhead as your tests adapt more gracefully to browser updates.

- **Boosted Automation Capabilities :** BiDi's key strength lies in its bi-directional communication and event-driven architecture. This allows for a more dynamic and responsive testing experience compared to the traditional approach. Your tests can react to events happening within the browser itself, leading to more robust and adaptable automation.

- **Seamless Cross-Browser Support :** BiDi is a W3C standard, meaning it strives for consistent implementation across different browsers. This eliminates the need to write and maintain separate test scripts for each browser you want to support. With LambdaTest's vast browser grid, you can leverage BiDi for wider test coverage with a single, unified test suite.

- **Fine-Grained Control over Browser Interactions :** BiDi offers access to lower-level browser functionalities that weren't readily available with traditional WebDriver. You can now interact with browser features like console logs and network traffic, providing finer control over the testing process. This can be particularly useful for debugging complex test scenarios or monitoring browser behavior in more detail.

- **Future-Proofing Your Test Suite :** BiDi represents the future of web browser automation. By adopting BiDi early on, you're future-proofing your test suite and ensuring compatibility with upcoming browser advancements that leverage this powerful protocol.

## Steps to run tests 

Following are the steps to run tests on LambdaTest using **WebdriverIO with BiDi Protocol**:

### Prerequisites
- Node.js >= 12
- Your LambdaTest [Username and Access Key](/support/docs/using-environment-variables-for-authentication-credentials/)

### Step 1: Setup the project

You can use your own project to configure and test it. For demo purposes, we are using the sample repository.

:::tip Sample repo
Download or Clone the code sample for the Selenium WebdriverIO BiDi from the LambdaTest GitHub repository to run the tests.

<a href="https://github.com/4DvAnCeBoY/wdio-bidi-tests" className="github__anchor"><img loading="lazy" src={require('../assets/images/icons/github.png').default} alt="Image" className="doc_img"/> View on GitHub</a>
:::

Install all the necessary dependencies of the project by running the following command:

```bash
npm install
```

### Step 2: Set up your LambdaTest credentials

- Create a `.env` file in the root folder of your project.
- Add your LambdaTest [Username and Access Key](/support/docs/using-environment-variables-for-authentication-credentials/) in place of `<YOUR_USERNAME>` and `<YOUR_ACCESS_KEY>`

```yaml
LT_USERNAME = <YOUR_USERNAME>
LT_ACCESS_KEY = <YOUR_ACCESS_KEY>
```

### Step 3: Trigger the tests

- Pass the `webSocketUrl` as true in the `wdio.lambdatest.conf.js` file to enable BiDi support.

  ```yaml
  webSocketUrl: true
  ```

- Run the following command in your terminal to trigger the tests on LambdaTest platform using the specified configuration.

  ```bash
  npm run wdio
  ```