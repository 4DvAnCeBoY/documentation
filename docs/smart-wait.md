---
id: smart-wait
title: SmartWait Functionality for Selenium Automation
hide_title: false
sidebar_label: SmartWait Functionality
description: Learn how to use SmartWait Functionality for your Selenium tests to increase the efficiency and accuracy of automated test execution. 
keywords:
- smart wait selenium
- smart wait selenium testing
- smart wait automation
url: https://www.lambdatest.com/support/docs/smart-wait/
site_name: LambdaTest
slug: smart-wait/
---
With LambdaTest's SmartWait feature, you can increase the efficiency and accuracy of automated test execution. Before performing any action on a webpage element, it conducts a series of actionability checks. By using an intelligent algorithm, SmartWait holds off on performing an action until all relevant checks have been successfully completed. It returns the appropriate Selenium error message if the checks are not passed within a predetermined timeframe.

You can use this feature to reduce the amount of code dedicated to explicit/implicit waits in your test suite, making it easier to read and maintain.

> **Note :** The **SmartWait** functionality is fully supported on HyperExecute as well, allowing you to leverage intelligent wait handling during parallel and distributed test executions.

## How SmartWait can help you?

SmartWait functionality can help you in multiple ways. Some of its benefits includes

- **Increased Accuracy**: SmartWait increases the accuracy of your test results by ensuring that actions are only executed on elements that are ready and actionable.
- **Code Optimization**: With SmartWait, your test scripts will have fewer explicit and implicit wait commands, thus making them easier to read and maintain.
- **Enhanced Efficiency**: Using the SmartWait feature, your test suite becomes more efficient by eliminating unnecessary waits and performing actions as soon as the elements are ready.
- **Intelligent Error Handling**: When actionability checks fail, SmartWait returns the relevant Selenium error, helping you identify and resolve issues more quickly.

## How to use SmartWait Functionality?
To use the SmartWait functionality, follow the below steps:

1. **Set SmartWait Time Limit :** Specify the maximum amount of time you want your test script to wait until an element becomes actionable. As per your test requirements, this time limit can be set.

```javascript
LT:Options {
...
"smartWait": 10 // It accepts integer values as second
"smartWaitRetryDelay": 1
...
}
```

:::info
- Min value of `smartWait` is 5 seconds and max is 120 seconds, default being 1 seconds.
- The capability `smartWaitRetryDelay` to define the time interval of retries. If not provided, default interval of 1 second is considered.
- Min value of `smartWaitRetryDelay` is 1 second and max is 4 seconds, default being 1 second.
:::

2. **Execute Test Suite :** As usual, run your test suite. Prior to executing each action on a webpage element, SmartWait automatically performs actionability checks.

3. **View Test Results :** Upon executing the test suite, view your results. SmartWait will have returned the relevant Selenium error message if any actionability checks failed within the predetermined timeframe.

LambdaTest's SmartWait feature enhances the capabilities of automated testing. SmartWait enhances the efficiency and accuracy of your testing processes by intelligently managing wait times and ensuring actions are executed at the most opportune time.
