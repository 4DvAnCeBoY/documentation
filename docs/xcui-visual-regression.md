---
id: xcui-visual-regression
title: Getting Started With Visual Regression Testing Using XCUI On SmartUI Real Devices
sidebar_label: XCUI
description: Dive into our detailed XCUI Visual Regression support documentation for step-by-step guidance! Efficiently perform visual testing, manage applications, and ensure your mobile apps are visually perfect before launch.
keywords:
  - Visual Regression
  - Visual Regression Testing Guide
  - Visual Regression Test Automation
  - Visual Regression Automation Testing
  - Running Visual Regression Tests
  - Visual Regression Testing Online
  - Run Visual Regression
  - Visual Regression Run Specific Test
  - Visual Regression Testing Environment
  - How to Run Visual Regression Tests

url: https://www.lambdatest.com/support/docs/xcui-visual-regression/
site_name: LambdaTest
slug: xcui-visual-regression/
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import {YOUR_LAMBDATEST_USERNAME, YOUR_LAMBDATEST_ACCESS_KEY} from "@site/src/component/keys";
import CodeBlock from '@theme/CodeBlock';
import NewTag from '../src/component/newTag';

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
          "name": "SmartUI-Hooks",
          "item": "https://www.lambdatest.com/support/docs/xcui-visual-regression/"
        }]
      })
    }}
></script>

XCUI (XCTest UI) is Apple's native UI testing framework used for testing iOS applications. It is part of the XCTest framework and allows developers to write UI automation tests for iOS apps. In this documentation, you will learn step-by-step how to perform regression testing and find Visual UI Regression bugs easily with the help of Smart Testing.

## Prerequisites

- Your LambdaTest [Username and Access key](https://accounts.lambdatest.com/security).
- Access to an **iOS** app (.ipa) and an **iOS Test** app (.ipa file).
- Go to [`LambdaTest SmartUI`](https://smartui.lambdatest.com/) and login along with your credentials.

<!-- :::tip
If you do not have any **Android** app (.apk) and an **Android Test** app (.apk) file, you can run your sample tests on LambdaTest by using our sample :link: [Android app](https://prod-mobile-artefacts.lambdatest.com/assets/docs/proverbial_android.apk) and a sample :link: [Espresso Test](https://prod-mobile-artefacts.lambdatest.com/assets/docs/proverbial_android_expressotest.apk).
::: -->

## Step 1: Create a SmartUI Project

The first step is to create a project with the application in which we will combine all your **builds** run on the project.
To create a SmartUI Project, follow these steps:

1. Go to [Projects page](https://smartui.lambdatest.com/)
2. Click on the `new project` button
3. Select the platform as <b>Real Device </b> for executing your `XCUI` tests.
4. Add name of the project, approvers for the changes found, tags for any filter or easy navigation.
5. Click on the **Submit**.

<!-- <img loading="lazy" src={require('../assets/images/uploads/smart-ui-1.webp').default} alt="cmd" width="768" height="373" className="doc_img"/> -->

## Step 2: Set up your Authentication

Now, you need to export your environment variables LT_USERNAME and LT_ACCESS_KEY that are available in the [LambdaTest Profile page](https://accounts.lambdatest.com/details/profile).

Run the below mentioned commands in your terminal to setup the CLI and the environment variables.

<Tabs className="docs__val">

<TabItem value="bash" label="Linux / MacOS" default>
  <div className="lambdatest__codeblock">
  <CodeBlock className="language-bash">
  {`export LT_USERNAME=${ YOUR_LAMBDATEST_USERNAME()} \\
export LT_ACCESS_KEY=${ YOUR_LAMBDATEST_ACCESS_KEY()}`}
</CodeBlock>
</div>

</TabItem>

<TabItem value="powershell" label="Windows" default>

  <div className="lambdatest__codeblock">
  <CodeBlock className="language-powershell">
  {`set LT_USERNAME=${ YOUR_LAMBDATEST_USERNAME()} \`
set LT_ACCESS_KEY=${ YOUR_LAMBDATEST_ACCESS_KEY()}`}
</CodeBlock>
</div>

</TabItem>
</Tabs>

<!-- ## Step 3: Update your App Configurations

> It should be in your app configurations then only you can perform the Espresso integration.

- In your `build.gradle` file, add the [lambdatest-espresso](https://central.sonatype.com/artifact/io.github.lambdatest/lambdatest-espresso) dependency:

```bash
implementation 'io.github.lambdatest:lambdatest-espresso:1.0.1'
```

- Initialize this dependency in your test classes. You can do it as follows:

```bash java
import io.github.lambdatest.LTApp;
public class BrowserTest {

  LTApp smartUIApp = new LTApp();
  
  @Test
  public void checkBrowserPageIsOpened() throws InterruptedException {
    String response = smartUIApp.screenshot("LT-Espresso-Test");
  }
}
```

Now build your application. -->

## Step 3: Upload your Application

To begin testing, upload your iOS application (.ipa file) to LambdaTest's servers. You'll use our **REST API** for this process.

- **Authentication :** You'll need your LambdaTest Username and AccessKey. Combine them in the format `Username:AccessKey`.
- **Uploading the App :** Use **cURL command** to send a request to our API. The request should include the path to your application file (**appFile**).

<Tabs className="docs__val">

<TabItem value="bash" label="Linux / MacOS" default>

  <div className="lambdatest__codeblock">
    <CodeBlock className="language-bash">
  {`curl -u "${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}" --location --request POST 'https://manual-api.lambdatest.com/app/uploadFramework' --form 'appFile=@"<PATH_OF_YOUR_IOS_APP>"' --form 'type="xcuit-ios"'`}
  </CodeBlock>
</div>

</TabItem>

<TabItem value="powershell" label="Windows" default>

  <div className="lambdatest__codeblock">
    <CodeBlock className="language-powershell">
{`curl -u "${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}" --location --request POST "https://manual-api.lambdatest.com/app/uploadFramework" --form "appFile=@"<PATH_OF_YOUR_IOS_APP>"" --form "type=\"xcuit-ios\""`}
  </CodeBlock>
</div>

</TabItem>
</Tabs>

:::info
- Provide the path of your ios application in the above URL in place of `<PATH_OF_YOUR_IOS_APP>`
- Response of above cURL will be a **JSON** object containing the `App URL` of the format - `lt://APP123456789123456789` and will be used in the last step.
:::

## Step 4: Upload Your Test Suite

Upload your XCUI test suite (.ipa) file to LambdaTest servers using our REST API.

The following sample cURL command shows how to upload a test suite:

<Tabs className="docs__val">

<TabItem value="bash" label="Linux / MacOS" default>

  <div className="lambdatest__codeblock">
    <CodeBlock className="language-bash">
  {`curl -u "${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}" --location --request POST 'https://manual-api.lambdatest.com/app/uploadFramework' --form 'appFile=@"<PATH_OF_YOUR_TEST_SUITE_APP>"' --form 'type="xcuit-ios"'`}
  </CodeBlock>
</div>

</TabItem>

<TabItem value="powershell" label="Windows" default>

  <div className="lambdatest__codeblock">
    <CodeBlock className="language-powershell">
{`curl -u "${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}" --location --request POST "https://manual-api.lambdatest.com/app/uploadFramework" --form "appFile=@"<PATH_OF_YOUR_TEST_SUITE_APP>"" --form "type=\"xcuit-ios\""`}
  </CodeBlock>
</div>

</TabItem>
</Tabs>

:::info
- Provide the path of your ios application in the above URL in place of `<PATH_OF_YOUR_TEST_SUITE_APP>`
- Response of above cURL will be a **JSON** object containing the `App URL` of the format - `lt://APP123456789123456789` and will be used in the last step.
:::

## Step 5: Executing The Test

- You will need **base64 encoded authentication** in order to execute your Espresso automation test suite. Enter your `username:accesskey` in **[Basic Authentication Header Generator](https://mixedanalytics.com/knowledge-base/api-connector-encode-credentials-to-base-64/)** to generate your auth token.

Take note of the base64 encoded authentication which needs to be added in the next step.

<div className="lambdatest__codeblock">
    <CodeBlock className="language-powershell">
{`${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}`}
  </CodeBlock>
</div>

- Once you have uploaded your app and test suite, you can execute your test by running the following command:
 
> Enter your **BASIC_AUTH_TOKEN**, **APP_ID** (generated in the fourth step) and **TEST_SUITE_ID** (generated in the fifth step) in the below command.

```javascript
curl --location 'https://mobile-api.lambdatest.com/framework/v1/xcui/build' \
--header 'Authorization: Basic BASIC_AUTH_TOKEN' \
--header 'Content-Type: application/json' \
--data '{
    "app" : "lAPP_ID", //enter your app-id
    "testSuite": "TEST_SUITE_ID", //enter your test-suite id
    "device" :  ["iPhone 13-16"], //enter your device names
    "smartUI.project": "XCUI-SmartUI-Project",
    "build" : "Proverbial-XCUITest",
    "video" : true,
    "queueTimeout": 10800,
    "idleTimeout": 150,
    "devicelog": true,
    "network": false,
    "only-testing" : ["LambdaUiKitIOSUITestsLaunchTests"],
    "smartUI.cropStatusBar" : true,
    "smartUI.cropNavigationBar" : true
}'
```

> You can check the executed builds over at [LambdaTest SmartUI](https://smartui.lambdatest.com/).

## Smart Crop With SmartUI

The all-new **Real Device mobile notification status bar and navigation bar crop** feature in SmartUI allows you to take your visual regression testing workflows to the next level. With Smart Crop, you can crop the status bar and navigation bar or footer from screenshots, enabling them to focus solely on the core UI elements during visual comparisons.

By leveraging machine learning algorithms, it accurately detects and crops the status bar and navigation bar from screenshots. With precise image processing techniques, SmartUI precisely identifies the location of status bar elements. By excluding it from visual comparisons, the focus is solely on critical UI elements.  

| Original Screenshot | Cropped Screenshot |
|---------------------|--------------------|
| <img loading="lazy" src={require('../assets/images/smart-visual-testing/screenshot.webp').default} alt="Profile" width="1360" height="603" className="doc_img"/> | <img loading="lazy" src={require('../assets/images/smart-visual-testing/cropped_ss.jpg').default} alt="Profile" width="1360" height="603" className="doc_img"/> |