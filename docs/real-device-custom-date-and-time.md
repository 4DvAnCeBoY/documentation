---
id: set-date-time-hour-format-real-devices
title: Set Custom Date, Time & Hour Format on Real Devices
sidebar_label: Date & Time Settings
description: Configure date, time, and hour-format on iOS and Android devices during manual and Appium-based automation testing on LambdaTest.

keywords:
  - set device time iOS
  - change date mobile automation
  - iOS 12-hour format testing
  - real device date time change
  - Appium date override
  - LambdaTest date configuration
  - real device time simulation
  - app testing on real device
  - simulate date time
  - iOS automation hooks
url: https://www.lambdatest.com/support/docs/set-date-time-hour-format-real-devices/
site_name: LambdaTest
slug: set-date-time-hour-format-real-devices/
---
import CodeBlock from '@theme/CodeBlock';
import {YOUR_LAMBDATEST_USERNAME, YOUR_LAMBDATEST_ACCESS_KEY} from "@site/src/component/keys";

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

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
      "name": "Set Date and Time on Real Devices",
      "item": "https://www.lambdatest.com/support/docs/set-date-time-hour-format-real-devices/"
    }]
  }) }}
></script>


Testing applications often requires validation across different date, time, and format scenarios. LambdaTest now supports dynamic configuration of **date, time, 12/24-hour format**, and **automatic time toggle** on real iOS and Android devices — both in **manual** sessions and via **Appium automation hooks**.

This enables use cases like testing scheduled alerts, AM/PM behaviors, time-bound features, and regional formatting validations.

---

## Access Date & Time Settings on LambdaTest Real Devices

**Step 1:** Log into your LambdaTest dashboard and navigate to **Real Devices** > **App Testing**.

**Step 2:** Select your desired app and an iOS device (iOS 14+), then click **Start** to launch your session.

**Step 3:** Once the session starts, open the **iOS Settings** tab in the left sidebar.

**Step 4:** Click on **Set Date and Time** to open the configuration modal. 

<img loading="lazy" src={require('../assets/images/real-device-app-testing/set-date-and-time-pic1.png').default} className="doc_img"/>

**Step 5:**  In the **modal**, configure the **date**, **time**, and **time format** as needed, then click **Update** to apply the changes to the device.

<img loading="lazy" src={require('../assets/images/real-device-app-testing/set-date-and-time-pic-last.png').default} className="doc_img"/>


---

## Date & Time Configuration Options

<img loading="lazy" src={require('../assets/images/real-device-app-testing/set-date-and-time-pic2.png').default} className="doc_img"/>

The modal includes four options to simulate various datetime-related behaviors:

### 1. Set Date and Time Automatically
- **Toggle ON:** Syncs the device with network time.
- **Toggle OFF:** Unlocks manual controls for custom configuration.
- Disabling this is mandatory to manually edit date or time.

<img loading="lazy" src={require('../assets/images/real-device-app-testing/set-date-and-time-pic4.png').default} className="doc_img"/>


### 2. Date
- Opens a calendar picker with selectable dates up to **7 days ahead**.
- Selecting a date updates the system date on the device.
- Past dates and dates beyond 7 days are **grayed out** and unselectable.
- An **Apply** button appears only when a valid date is selected.

<img loading="lazy" src={require('../assets/images/real-device-app-testing/set-date-and-time-pic3.png').default} className="doc_img"/>


### 3. Time
- Allows custom time entry in `HH:MM:SS` format.
- Picker adjusts based on selected hour-format (12 or 24-hour).
- Supports both **manual typing** and **arrow key navigation** for time input.

### 4. Time Format (12/24 Hour)
- Choose between **12-hour** (AM/PM toggle) and **24-hour** formats.
- 12-hour format shows AM/PM option in time picker.
- 24-hour format disables AM/PM selection automatically.

<img loading="lazy" src={require('../assets/images/real-device-app-testing/set-date-and-time-pic-5.png').default} className="doc_img"/>

---

## Configure Date & Time via Appium

You can configure date, time, time format (12h/24h), and toggle automatic syncing via a LambdaTest custom Appium executor hook.

### Appium Hook:

```js
lambda_executor: { "action": "updateDeviceSettings", "arguments": { "customDate": "Jun 20 2025", "customTime": "15:05", "twelveHourTime": "On", "setAutomatically": "On" } } 
```


### Appium Hook:

| Argument           | Format        | Description                                                                  |
| ------------------ | ------------- | ---------------------------------------------------------------------------- |
| `customDate`       | `MMM DD YYYY` | Future-only date. Max 7 days from current date.                              |
| `customTime`       | `HH:MM`       | Time in 24-hour format. Interpreted based on selected hour format.           |
| `twelveHourTime`   | `On` / `Off`  | Toggles between 12-hour (`On`) and 24-hour (`Off`) formats.                  |
| `setAutomatically` | `On` / `Off`  | Enables or disables syncing time with network. Disabling allows manual edit. |

---

## Supported Platforms: 

| Platform | Configuration Methods       | OS Versions Supported |
| -------- | --------------------------- | --------------------- |
| iOS      | Manual + Appium Executor    | iOS 14 and above      |
| Android  | Manual Only (No automation) | Android 10 and above  |


---

## Use Cases: 

- Test scheduled notifications and alerts
- Validate time-sensitive app flows
- Check 12/24-hour format compatibility
- Simulate future or custom dates
- Debug calendar and time-based modules
- Verify auto/manual time toggle behavior
- Test date/time edge cases (e.g., midnight, EOM)
