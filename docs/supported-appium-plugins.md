---
id: supported-appium-plugins
title: Supported Appium Plugins
hide_title: false
sidebar_label: Supported Appium Plugins
description: This document provides information about configuring Appium plugins for tests on the LambdaTest platform and also provides a list of supported plugins.

keywords:
 - appium
 - appium languages
 - appium framework 
 - configuration
 - plugins
 - images plugin
 - test automation frameworks
 - app testing
 - lambdaTest 

url: https://www.lambdatest.com/support/docs/supported-appium-plugins/
site_name: LambdaTest
slug: supported-appium-plugins/
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
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
          "name": "Appium Testing ",
          "item": "https://www.lambdatest.com/support/docs/supported-appium-plugins/"
        }]
      })
    }}
></script>
Enhance your testing experience on LambdaTest by leveraging a variety of Appium plugins. Plugins offer various ways to extend or modify Appium's behavior. They are completely optional and are not needed for standard automation functionality, but you may find them useful for more specialized automation workflows.
By using these plugins, you can tailor your testing environment to better suit your project's specific needs, leading to more efficient and effective test automation.

## Supported Plugins

Below is a list of the supported Appium plugins on LambdaTest:

| Plugin Name |  Description | Example |
|-------------|--------------|---------|
| `images`| Enables image comparison features in tests. Allows for verification of visual elements through images. | "appiumPlugins": ["images"] |
| `element-wait`| Provides enhanced wait capabilities for elements, allowing tests to wait for elements to be in a certain state.For further details, please check [this documentation](https://github.com/AppiumTestDistribution/appium-wait-plugin). | "appiumPlugins": ["element-wait"] |
| `gestures` | Adds support for gesture-based interactions, enabling tests to perform complex gestures like swipe, pinch, and zoom. For further details, please check [this documentation](https://github.com/AppiumTestDistribution/appium-gestures-plugin). | "appiumPlugins": ["gestures"]
| `ocr`| Enables Optical Character Recognition (OCR) capabilities for detecting and interacting with on-screen text in images or video frames during tests. | "appiumPlugins": ["ocr"] |
| `execute-driver`| Allows the execution of custom scripts within the Appium driver context, giving enhanced flexibility and control during test execution. For more details, check [this documentation](https://www.npmjs.com/package/@appium/execute-driver-plugin) | "appiumPlugins": ["execute-driver"] |

**Python Example:**

```python
capabilities = {
    "appiumVersion": "2.2.1",
    "platformName": "iOS",
    "appiumPlugins": ["images", "element-wait", "gestures","ocr","execute-driver"],
    # Add other capabilities as needed
}
```

:::note 
- Appium plugins are only supported with version 2.0.0 and above appium versions. Please ensure that the `appiumVersion` capability is set correctly to utilize these plugins.
:::