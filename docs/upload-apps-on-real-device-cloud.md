---
id: upload-apps-on-real-device-cloud
title: Upload Apps on LambdaTest’s Real Device Cloud
hide_title: true
sidebar_label: Uploading Apps
description: With LambdaTest, perform live interactive testing of mobile applications on Android emulators and iOS simulators and ensure your apps work seamlessly across multiple versions of Android emulators and iOS simulators.
keywords:
- upload apps on real device cloud 
- real device cloud
- uploading apps 
url: https://www.lambdatest.com/support/docs/upload-apps-on-real-device-cloud/
site_name: LambdaTest
slug: upload-apps-on-real-device-cloud/
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

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
          "name": "Support",
          "item": "https://www.lambdatest.com/support/docs/"
        },{
          "@type": "ListItem",
          "position": 3,
          "name": "Native Mobile App Testing",
          "item": "https://www.lambdatest.com/support/docs/upload-apps-on-real-device-cloud/"
        }]
      })
    }}
></script>

# Upload Apps on LambdaTest’s Real Device Cloud

LambdaTest allows you to upload applications either from your local system or directly from a public URL for testing on real Android and iOS devices. This ensures that your apps perform optimally across diverse user environments.

Let's dive in to learn how to upload apps to the Real Device Cloud.

***

## Supported Files and Sizes

<Tabs className="docs__val">
  <TabItem value="android" label="Android" default>
Upload the .apk, .aab files of your app from your system or from a public URL and ensure the size of the files is not more than 1 GB.
</TabItem>
<TabItem value="iOS" label="iOS" default>
Upload the .ipa files of your app from your system or from a public URL and ensure the size of the files is not more than 1 GB.
</TabItem>
</Tabs>

## How to Upload Apps

**From Your System:** Select the **Upload** button to add an application from your system.

**Via URL:** If your app is hosted online, you can also upload it by simply entering its public URL in the designated **Upload via URL** field.

<img loading="lazy" src={require('../assets/images/mobile-app-testing/upload-through-url.webp').default} alt="Native Mobile App Testing"  className="doc_img" width="1366" height="629"/>

**Via API:** Upload apps via API onto the real device dashboard. Check out our detailed [support documentation](https://www.lambdatest.com/support/docs/app-testing-apis/#uploading-your-application) to learn how to upload apps via API. 

## Sharing Apps

If you want to share any app with your team members, simply click on the checkbox and then upload the app. The newly uploaded app will be visible for all the team members in their dashboards.

<img loading="lazy" src={require('../assets/images/mobile-app-testing/share-apps-with-team-members.webp').default} alt="Real "  className="doc_img" width="1366" height="629"/>

Once your app is uploaded, you can see various app details such as App Name, Version, Bundle ID for iOS devices, App Package for android devices, the time and name of the person by whom it was uploaded. 

<img loading="lazy" src={require('../assets/images/mobile-app-testing/app-details.webp').default} alt="Real "  className="doc_img" width="1366" height="629"/>

## App Settings

You can customize the app settings based on your app requirements and testing scenarios.
Hover over the app, click on the settings icon for the app settings to open.

<img loading="lazy" src={require('../assets/images/mobile-app-testing/app-settings.webp').default} alt="Real "  className="doc_img" width="1366" height="629"/>

- Set the **App Name** to easily identify it on the dashboard.

- Use the **App ID** provided by Lambdatest to execute your automation scripts.

- Control **Visibility** to manage who in your team can view or edit the app.

- Use the **App Version Code** to differentiate between different builds.

You can edit the information at any time and save the changes. If an app is no longer needed, you have the option to delete it permanently from your account.

Check out our detailed support documentation to learn in detail about the app setting features.

<nav aria-label="breadcrumbs">
  <ul className="breadcrumbs">
    <li className="breadcrumbs__item">
      <a className="breadcrumbs__link" href="https://www.lambdatest.com">
        Home
      </a>
    </li>
    <li className="breadcrumbs__item">
      <a className="breadcrumbs__link" target="_self" href="https://www.lambdatest.com/support/docs/">
        Support
      </a>
    </li>
    <li className="breadcrumbs__item breadcrumbs__item--active">
      <span className="breadcrumbs__link">
        Real Device App Testing
      </span>
    </li>
  </ul>
</nav>