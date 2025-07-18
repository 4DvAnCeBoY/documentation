---
id: hyperexecute-detox-testing
title: Detox Testing on HyperExecute
hide_title: false
sidebar_label: Detox
description: Learn how to run Detox automation tests on HyperExecute for React Native apps
keywords:
  - Detox
  - Detox automation
  - Detox testing
  - detox testing react native
  - detox automation testing
  - detox lambdatest
  - hyperexecute
  - hyperexecute detox testing
  - detox tests on hyperexecute
  - hyperexecute automation testing
  - HyperExecute React Native automation
url: https://www.lambdatest.com/support/docs/hyperexecute-detox-testing/
site_name: LambdaTest
slug: hyperexecute-detox-testing/
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
          "name": "How to run Detox automation tests on HyperExecute",
          "item": "https://www.lambdatest.com/support/docs/hyperexecute-detox-testing/"
        }]
      })
    }}
></script>

Detox is a popular end-to-end testing framework for React Native applications. This documentation will help you run your Detox tests on LambdaTest HyperExecute using your local system setup.

## Run a Sample Project
### Step 1: Clone Sample Repository

:::tip Detox repo
Download or Clone the Detox sample from LambdaTest’s GitHub Repository

<a href="https://github.com/LambdaTest/LT-detox" className="github__anchor"><img loading="lazy" src={require('../assets/images/icons/github.png').default} alt="Image" className="doc_img"/> View on GitHub</a>
:::

### Step 2: Download the CLI in your Project
Download the HyperExecute CLI and copy it into the root folder of the downloaded sample repository.

| Platform | HyperExecute CLI |
| ---------| ---------------- |
| Linux | https://downloads.lambdatest.com/hyperexecute/linux/hyperexecute |
| Windows | https://downloads.lambdatest.com/hyperexecute/windows/hyperexecute.exe |
| macOS | https://downloads.lambdatest.com/hyperexecute/darwin/hyperexecute |

### Step 3: Execute your Test Suite
From the project root directory, execute the below CLI command in your terminal:

<div className="lambdatest__codeblock">
  <CodeBlock className="language-bash">
    {`./hyperexecute --user ${ YOUR_LAMBDATEST_USERNAME()} --key ${ YOUR_LAMBDATEST_ACCESS_KEY()} --config RELATIVE_PATH_OF_YOUR_YAML_FILE `}
  </CodeBlock>
</div>

> **NOTE :** In case of macOS, if you get a permission denied warning while executing CLI, simply run **`chmod u+x ./hyperexecute`** to allow permission. In case you get a security popup, allow it from your **System Preferences** → **Security & Privacy** → **General tab**.

<img loading="lazy" src={require('../assets/images/hyperexecute/frameworks/Detox/Detox_cmd.png').default} alt="TestNG HyperExecute Terminal Logs"  width="1920" height="868" className="doc_img"/>

<br /><br />

You've successfully triggered the Detox tests on HyperExecute. Visit the [HyperExecute Dashboard](https://hyperexecute.lambdatest.com/hyperexecute) and check your Job status. 

## Configure your own Project

### Step 1: Download the CLI in your Project
Download the HyperExecute CLI and copy it into the root folder.

| Platform | HyperExecute CLI |
| ---------| ---------------- |
| Linux | https://downloads.lambdatest.com/hyperexecute/linux/hyperexecute |
| Windows | https://downloads.lambdatest.com/hyperexecute/windows/hyperexecute.exe |
| macOS | https://downloads.lambdatest.com/hyperexecute/darwin/hyperexecute |

### Step 2: Configure YAML in your Test Suite
Use the sample YAML below to configure your execution:

```yaml reference title="hyperexecute.yaml"
https://github.com/LambdaTest/LT-detox/blob/main/yaml/hyperexecute.yaml
```

> 📘 To explore more configuration options and tailor settings to your project needs, check out the [YAML documentation](https://www.lambdatest.com/support/docs/hyperexecute-yaml-parameters/).

### Step 3: Monitor the Test Execution

Visit the [HyperExecute Dashboard](https://hyperexecute.lambdatest.com/hyperexecute) and check your Job status. 

<img loading="lazy" src={require('../assets/images/hyperexecute/frameworks/Detox/Detox_dashboard.png').default} alt="TestNG HyperExecute Terminal Logs"  width="1920" height="868" className="doc_img"/>

You can click on **View Test** from the **HyperExecute logs**, which will take you to the [App Automation dashboard](https://appautomation.lambdatest.com/build). There, you can access detailed **device logs**, **crash logs**, and **Metadata** for your test. You’ll also be able to watch a **video recording** of the Test sessions for better **debugging** and **analysis**.

> For any query or doubt, please feel free to contact us via <span className="doc__lt" onClick={() => window.openLTChatWidget()}>**24×7 chat support**</span> or you can also drop a mail to **support@lambdatest.com**.<br />