---
id: hyperexecute-testim-integration
title: Integrate Testim with HyperExecute
hide_title: false
sidebar_label: Testim
description:  Testim, a test case management tool, and HyperExecute, a cloud-based test execution platform streamline your testing process by efficiently managing test cases.
keywords:
  - LambdaTest Hyperexecute
  - LambdaTest Hyperexecute help
  - LambdaTest Hyperexecute documentation
  - testim
  - Integrations
  - Products
url: https://www.lambdatest.com/support/docs/hyperexecute-testim-integration/
site_name: LambdaTest
slug: hyperexecute-testim-integration/
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
          "name": "Integration with Products",
          "item": "https://www.lambdatest.com/support/docs/hyperexecute-testim-integration/"
        }]
      })
    }}
></script>

Testim is a AI Native test authoring platform designed to automate software testing, particularly web and mobile applications. It focuses on creating stable and reliable automated tests. It allows creating tests without writing code or by incorporating custom JavaScript for more intricate scenarios. You can manage and scale the test automation process efficiently, which is particularly valuable for Agile development teams.

This document details the seamless integration between HyperExecute and Testim, enabling you to run your automated tests.

## Prerequisite

- You will need your Testim account.
- LambdaTest account. You can [sign up for free](https://accounts.lambdatest.com/dashboard).
- LambdaTest [Username and Access Key](/support/docs/hyperexecute-how-to-get-my-username-and-access-key/)

## Step 1: Setup the Grid

- Click on your profile icon >> **Grids** button.
- Click on **Add New Grid** button >> select **LambdaTest** as your Grid Type and click on **Next** button.
- Configure your Grid:
    - Enter the name of your Grid.
    - Update your Host and Port number.
    - Enter your LambdaTest Username and Access Key >> click on **Add** button.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/hyperexecute/integration/products/testim/grid-setup.mp4').default} type="video/mp4" />
</video>

## Step 2: Record your Tests

- Click on the **New Test** button >> **Start Recording** button.
- Enter your app URL >> click on **Create Test**.
- It will start recording the tests. After your testing is completed, stop the recording and save your test.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/hyperexecute/integration/products/testim/test-record.mp4').default} type="video/mp4" />
</video>

## Step 3: Configure your Test to execute from CLI

- Go to the **Settings** >> select the **CLI** tab.
- You will find the sample command >> copy that and paste it in the `testRunnerCommand` in your YAML file.

## Step 4: Configure your YAML

Create an empty folder, inside which create your YAML file to trigger the test.

- In the `pre` flag, enter the command to download the testim cli.
- In the `testRunnerCommand`, enter your runner command copied in the previous step.

```yaml
---
version: 0.1
globalTimeout: 150
testSuiteTimeout: 150
testSuiteStep: 150

runson: mac

pre: 
  - npm i -g @testim/testim-cli

runtime:
  language: node
  version: "18.0.0"

autosplit: true

concurrency: 1

testDiscovery:
 type: raw
 mode: static
 command: echo "HYP with Testim"

testRunnerCommand: ./.hyperexecute/snooper --frameWork testim --testimProject YOUR_PROJECT_ID --testimToken YOUR_TESTIM_TOKEN --testimProjectBranch YOUR_BRANCH_NAME
```

## Step 5: Setup the CLI

After configuring your YAML file, you need to setup the CLI and the environment variables.

### Download the HyperExecute CLI

The CLI is used for triggering the tests on HyperExecute. It is recommend to download the CLI binary on the host system and keep it in the root directory of the suite to perform the tests on HyperExecute.

You can download the CLI for your desired platform from the below mentioned links:

| Platform | HyperExecute CLI |
| ---------| ---------------- |
| Windows | https://downloads.lambdatest.com/hyperexecute/windows/hyperexecute.exe |
| MacOS | https://downloads.lambdatest.com/hyperexecute/darwin/hyperexecute |
| Linux | https://downloads.lambdatest.com/hyperexecute/linux/hyperexecute |

### Setup Environment Variable

Now, you need to export your environment variables *LT_USERNAME* and *LT_ACCESS_KEY* that are available in the [LambdaTest Profile page](https://accounts.lambdatest.com/detail/profile).

Run the below mentioned commands in your terminal to setup the CLI and the environment variables.

<Tabs className="docs__val">

<TabItem value="bash" label="Linux / MacOS" default>

  <div className="lambdatest__codeblock">
    <CodeBlock className="language-bash">
  {`export LT_USERNAME="${ YOUR_LAMBDATEST_USERNAME()}"
export LT_ACCESS_KEY="${ YOUR_LAMBDATEST_ACCESS_KEY()}"`}
  </CodeBlock>
</div>

</TabItem>

<TabItem value="powershell" label="Windows" default>

  <div className="lambdatest__codeblock">
    <CodeBlock className="language-powershell">
  {`set LT_USERNAME="${ YOUR_LAMBDATEST_USERNAME()}"
set LT_ACCESS_KEY="${ YOUR_LAMBDATEST_ACCESS_KEY()}"`}
  </CodeBlock>
</div>

</TabItem>
</Tabs>

## Step 6: Execute your Test

> **NOTE :** In case of MacOS, if you get a permission denied warning while executing CLI, simply run **`chmod u+x ./hyperexecute`** to allow permission. In case you get a security popup, allow it from your **System Preferences** → **Security & Privacy** → **General tab**.

Run the below command in your terminal at the root folder of the project:

```bash
./hyperexecute --config RELATIVE_PATH_OF_YOUR_YAML_FILE
```

OR use this command if you have not exported your username and access key in the step 2.

<div className="lambdatest__codeblock">
  <CodeBlock className="language-bash">
    {`./hyperexecute --user ${ YOUR_LAMBDATEST_USERNAME()} --key ${ YOUR_LAMBDATEST_ACCESS_KEY()} --config RELATIVE_PATH_OF_YOUR_YAML_FILE `}
  </CodeBlock>
</div>