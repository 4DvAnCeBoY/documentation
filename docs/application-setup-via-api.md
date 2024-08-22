---
id: application-setup-via-api
title: Perform Operations on your Application via API
sidebar_label: via API
description: This guide will explain how to perform operations with your applications via api for real and virtual devices.
keywords:
  - appium
  - application operations
  - lambdatest
  - mobile testing
  - apis
  - setup application
url: https://www.lambdatest.com/support/docs/application-setup-via-api/
site_name: LambdaTest
slug: application-setup-via-api/
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import {YOUR_LAMBDATEST_USERNAME, YOUR_LAMBDATEST_ACCESS_KEY} from "@site/src/component/keys";
import CodeBlock from '@theme/CodeBlock';

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
          "name": "Applications",
          "item": "https://www.lambdatest.com/support/docs/application-setup-via-api/"
        }]
      })
    }}
></script>
To test your **iOS** (.ipa file) or **Android** (.apk or .aab file) application on LambdaTest, you can use our public REST APIs. In this documentation, we have listed all the operations you can perform with your application via APIs or cURL commands for both Virtual and Real Devices.

:::note
The maximum size for application should not exceed 1GB.
:::

:::tip
- If you do not have any **.apk** or **.ipa** file, you can run your sample tests on LambdaTest by using our sample :link: [Android app](https://prod-mobile-artefacts.lambdatest.com/assets/docs/proverbial_android.apk) or sample :link: [iOS app](https://prod-mobile-artefacts.lambdatest.com/assets/docs/proverbial_ios.ipa).
:::

## Upload your Application

| PARAMETER | EXAMPLE | DESCRIPTION |
|-----------------|-------------|------------|
| `custom_id` | `-F "custom_id="Proverbial_1.0"` | You do not have to remember the `app_URL` and only use the `custom_id` to run your automation on the same app. |
| `storage` | `-F "storage=file"` <br/> DEFAULT: `url` | Used to change the way LambdaTest stores the link. <br/> Used when we Upload using App URL |
| `visibility` | `-F "visibility=team"` <br/> DEFAULT: `individual` | Used to change the visibility of the application being uploaded. Once the app is uploaded using the `team`, everyone in the organisation can use the same URL to run the tests. |

### Using App File:

<div className="lambdatest__codeblock">
<CodeBlock className="language-bash">
{`curl -u "${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}" -X POST "https://manual-api.lambdatest.com/app/upload/realDevice" -F "appFile=@"/Users/macuser/Downloads/Appname.apk"" -F "name="appname""
`}
</CodeBlock>
</div>

### Using App URL:

<div className="lambdatest__codeblock">
<CodeBlock className="language-bash">
{`curl -u "${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}" -X POST "https://manual-api.lambdatest.com/app/upload/realDevice" -F "url=https://prod-mobile-artefacts.lambdatest.com/assets/docs/proverbial_android.apk" -F "name=Proverbial_App" -F "custom_id=sampleName" -F "storage=url" -F "visibility=individual"`}
</CodeBlock>
</div>

- Response of above cURL will be a **JSON** object containing the `App URL` of the format - ``lt://APP123456789123456789``

:::warning note
The upload time of your application can range from a few seconds to a minute, depending on the size of your application. Therefore, do not interrupt the cURL command request until you receive the response.
:::

## Fetch your Applications

<Tabs className="docs__val">

<TabItem value="android" label="Android" default>
  <div className="lambdatest__codeblock">
    <CodeBlock className="language-bash">
  {`curl --location --request GET "https://${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}@manual-api.lambdatest.com/app/data?type=android&level=user"`}
  </CodeBlock>
</div>

</TabItem>

<TabItem value="ios" label="iOS" default>
  <div className="lambdatest__codeblock">
    <CodeBlock className="language-powershell">
  {`curl --location --request GET "https://${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}@manual-api.lambdatest.com/app/data?type=ios&level=user"`}
  </CodeBlock>
</div>

</TabItem>
</Tabs>

Shown below is the response to the above cURL request.

```javascript
{
  "metaData": {
    "type": "ios",
    "total": 1
  },
  "data": [
    {
      "app_id": "APP100245789181570497850",
      "name": "proverbial_ios.ipa",
      "type": "ios",
      "updated_at": "2022-05-10T11:19:30.000Z",
      "shared": false,
      "source": "web-client"
    }
  ]
}
```

## Deleting your Application

To delete your uploaded apps, run the below cURL command. 

<div className="lambdatest__codeblock">
<CodeBlock className="language-bash">
{`curl --location --request DELETE "https://${ YOUR_LAMBDATEST_USERNAME()}:${ YOUR_LAMBDATEST_ACCESS_KEY()}@manual-api.lambdatest.com/app/delete" \
--header 'Content-Type: application/json' \
--data-raw '{
    "appIds" : "APPID1,APPID2"
}'
`}
</CodeBlock>
</div>

Shown below is the response to the above cURL request.

```javascript
{
  "message": "Deleted successfully."
}
```

## Processing check for your Application

To unlock features such as network logs, image injection, and screenshotunblock feature for your application, app needs to undergo a processing phase. This processing takes a few minutes after the application is uploaded. You can verify if the processing is complete before running your automation script using the following API.

<div className="lambdatest__codeblock">
<CodeBlock className="language-bash">
{`curl --location --request POST 'https://mobile-api.lambdatest.com/mobile-automation/api/v1/fetchpatchedapkurl' \
--header 'Authorization: Basic c2hhbnRhbnV3OkFPOEh3NHJtV2hxUlJZSVl3OEk1elMzajhCS0c2ZHl3SVBZeXNNSDJPakdtbFVheXZC' \
--header 'Content-Type: application/json' \y
--data-raw '{
    "appId": "APP10160161171698993659206876",
    "imageInjectionEnabled": true,
    "screenshotUnblockEnabled": true
}'`}
</CodeBlock>
</div>

The payload allows you to check the processing status for specific features. If the **patched_url** is empty, the processing is still in progress. To check if the processing for image injection or screenshot unblock is complete, pass either **imageInjectionEnabled** or **screenshotUnblockEnabled** as `true` based on the feature you are testing.

```javascript
{
    "data": {
        "imageinjection_ready": false, //current processing status
        "patched_url": "",
        "screenshotunblock_ready": false, //current processing status
        "status": "success"
    },
    "status": "success"
}
```