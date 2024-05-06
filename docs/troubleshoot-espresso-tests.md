---
id: troubleshoot-espresso-tests
title: Troubleshoot Your Espresso Tests
hide_title: false
sidebar_label: Troubleshoot Espresso Tests
description: Learn how to troubleshoot Espresso tests for your mobile applications to resolve different kinds of bugs for your failed test builds.
keywords:
- debug espresso tests
- how to debug espresso tests
- mobile app testing
url: https://www.lambdatest.com/support/docs/troubleshoot-espresso-tests/
site_name: LambdaTest
slug: troubleshoot-espresso-tests/
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
          "name": "Troubleshoot your Espresso Tests",
          "item": "https://www.lambdatest.com/support/docs/troubleshoot-espresso-tests/"
        }]
      })
    }}
></script>

This document is a guide to troubleshooting common errors encountered when running Espresso tests on LambdaTest. Espresso is an open-source Android UI testing framework that helps you automate tests for your mobile applications. Understanding these errors and their explanations can help you diagnose and resolve issues during your test execution on LambdaTest.

## Espresso Build Errors

This table highlights the errors encountered when running tests on [LambdaTest Real Devices without shards](/support/docs/getting-started-with-espresso-testing/).

<img loading="lazy" src={require('../assets/images/debug-espresso-test/5.png').default} alt="Image" width="1347" Height="610" className="doc_img"/> <br />

| Build Execution Errors | Root Cause of Error |
|--------------------------------------------|--------------------------|
|Application under test provided by you did not get installed. Please check the application.| The target application failed to install on the selected device during test execution. This indicates an issue with the provided application file or incompatibility with the chosen device configuration.| 
|Test Suite provided by you did not get installed. Please check the application.| This indicates that the test suite you provided could not be installed on the chosen LambdaTest environment. This might be due to invalid test suite files, incompatibility issues, or missing dependencies.| 
|Failed to fetch runner class for test extraction. Please recheck your test suite.| Test discovery failed. The system couldn't extract test cases or classes from the provided test suite application. This might be due to issues with the test suite app itself or its configuration.| 
|Failed to extract classes or tests from runner app - test discovery failed.| Test discovery failed. The system couldn't extract test cases or classes from the provided runner application. This might be due to issues with the test suite app itself or an incompatibility with the testing framework used. | 
|No tests found in the test suite. Please check your test suite or applied filters.| The test execution framework couldn't locate any test cases to run due to: <br /> <b>Empty Test Suite: </b>Ensure your test suite contains at least one test class with a @Test annotated method.<br /> <b>Incorrect Filtering: </b>Verify that any applied test filters aren't accidentally excluding all tests. You can see more on espresso test filtering [here](/support/docs/speedup-espresso/).| 
|Tests could not be run as localization setup failed. Please check locale and try again.| The test suite encountered a localization setup error. This means the system's locale or language settings could not be configured correctly. Please verify your locale settings and try re-running the tests. | 
|Oops! An error occurred at our end. Please try again.| A temporary infrastructure issue arose. While a device was allocated for your test, it became unavailable before the test execution started. Please retry the test or reach out to support@lambdatest.com if the issue persists. | 
|Desired Capabilities Error. Please check the desired capabilities that you have passed.| The test encountered a [`Desired Capabilities`](/support/docs/getting-started-with-espresso-testing/#capabilities-supported) Error.  This indicates an issue with the configuration provided for the test execution.  Please verify the values you have set for desired capabilities like device, platform, or application path. | 

## Espresso via HyperExecute Shard Errors

This table highlights the errors encountered when running espresso tests with [Shards via HyperExecute](/support/docs/sharding-espresso-rd-hyperexecute/) on LambdaTest Real Device Cloud.

<img loading="lazy" src={require('../assets/images/debug-espresso-test/4.png').default} alt="Image" width="1347" Height="610" className="doc_img"/> <br />

| Shard Execution Errors | Root Cause of Error |
|--------------------------------------------|--------------------------|
|Application under test provided by you did not get installed. Please check the application.| The target application failed to install on the selected device during test execution. This indicates an issue with the provided application file (APK/IPA) or incompatibility with the chosen device configuration.| 
|Test Suite provided by you did not get installed. Please check the application.| This indicates that the test suite you provided could not be installed on the chosen LambdaTest environment. This might be due to invalid test suite files, incompatibility issues, or missing dependencies.| 
|Failed to fetch runner class for test extraction. Please recheck your test suite.| Test discovery failed. The system couldn't extract test cases or classes from the provided runner application. This might be due to issues with the runner app itself or its configuration.| 
|Failed to extract classes or tests from runner app - test discovery failed.| Test discovery failed. The system couldn't extract test cases or classes from the provided runner application. This might be due to issues with the runner app itself or an incompatibility with the testing framework used. | 
|No tests found in the test suite. Please check your test suite or applied filters.| The test execution framework couldn't locate any test cases to run due to: <br /> <b>Empty Test Suite: </b>Ensure your test suite contains at least one test class with a @Test annotated method.<br /> <b>Incorrect Filtering: </b>Verify that any applied test filters aren't accidentally excluding all tests. You can see more on espresso test filtering [here](/support/docs/speedup-espresso/).| 
|Tests could not be run as localization setup failed. Please check locale and try again.| The test suite encountered a localization setup error. This means the system's locale or language settings could not be configured correctly. Please verify your locale settings and try re-running the tests. | 
|Oops! An error occurred at our end. Please try again.| A temporary infrastructure issue arose. While a device was allocated for your test, it became unavailable before the test execution started. Please retry the test. | 
|Desired Capabilities Error. Please check the desired capabilities that you have passed.| The test encountered a [`Desired Capabilities`](/support/docs/getting-started-with-espresso-testing/#capabilities-supported) Error.  This indicates an issue with the configuration provided for the test execution.  Please verify the values you have set for desired capabilities like device, platform, or application path. | 
| Oops! An error occurred at our end. Please try again. | An internal error occurred while retrieving configuration details for the test execution environment (HyperExecute API).  A temporary glitch might be preventing communication with the API. Please retry the test execution. If the issue persists, contact support for further assistance. |
|Build has been stopped. | The build process was terminated prematurely. User intervention caused this stoppage, likely due to errors encountered during the build phase. |
|Build breached queue timeout| The test execution encountered a "Build breached queue timeout" error. This indicates the build exceeded the maximum allowed wait time while in a queue. This could be due to high system load or insufficient resources on the LambdaTest platform. |