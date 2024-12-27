---
id: hyperexecute-slack-integration
title: Receive Instant Notification on your Jobs Directly in your Slack
hide_title: false
sidebar_label: Slack
description:  Streamline testing & communication! Integrate LambdaTest HyperExecute with Slack for real-time test notifications & updates. 
keywords:
  - LambdaTest Hyperexecute
  - LambdaTest Hyperexecute help
  - LambdaTest Hyperexecute documentation
  - slack
  - Integrations
  - Products
  - Automated testing alerts
  - DevOps communication
url: https://www.lambdatest.com/support/docs/hyperexecute-slack-integration/
site_name: LambdaTest
slug: hyperexecute-slack-integration/
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
          "name": "Integration with Products",
          "item": "https://www.lambdatest.com/support/docs/hyperexecute-slack-integration/"
        }]
      })
    }}
></script>

This document details the seamless integration between HyperExecute and Slack, enabling you to streamline your workflow and stay informed about your automated tasks. Through this integration, you can receive real-time notifications and crucial job details directly within your Slack workspace.

## Prerequisite

- An active LambdaTest account with Admin or User-level access. 
- Set up a dedicated Slack channel where you want to receive notifications from HyperExecute.

## Step 1: Navigate to the Integration Page

- Login to your LambdaTest Account.
- Navigate to the **Settings** > **Integration** page.
- Select the **Communication** tab and search for Slack.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/hyperexecute/integration/products/slack/1.mp4').default} type="video/mp4" />
</video>

## Step 2: Integrate the Slack with your LambdaTest Account

- Click on the **Connect** button and then **Install** for the Slack integration.

> **NOTE :** If you are already logged into Slack, you'll be redirected to a page where you have to post to a channel to confirm your identity or else you will be asked to provide Slack URL of your workspace.

- Select the channel you want to post on. Click on **Allow** button.

A notification would be shared on to all the members belonging to that channel, informing about your integration.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/hyperexecute/integration/products/slack/2.mp4').default} type="video/mp4" />
</video>

## Step 3: Update the Notification Settings and Trigger the Job

Once you integrate Slack, you need to configure notification settings to get test automation notifications on your integrated Slack channel.

- Click on the **Settings** button.
- Choose your **Notification Preferences** like Screenshot test completion messages, Build completion messages, etc.
- Update the **Notification Time** as well.
- Now run the test and visit the Slack channel to view the build notification containing Job Number, Job Status, Executed By, Started At, Job Duration, Test Duration etc.

## Receive Notification on Custom Slack Channels
> - To avail this feature, connect with our <span className="doc__lt" onClick={() => window.openLTChatWidget()}>Support Team.</span>
> - This feature does not work for **private** Slack channels.

After successfully integrating Slack, specify the Slack channel where you want Job updates to be sent by updating your HyperExecute YAML file:

```yaml title="hyperexecute.yaml"
slackChannel: hyperexecute-job-updates #slack channel name
```

Or, if you prefer using variable:

```yaml title="hyperexecute.yaml"
slackChannel: ${channel}
```

And then in your CLI/terminal, pass your desired channel name like:

```yaml
./hyperexecute --vars "channel=hyperexecute-job-updates" #enter your slack channel name
```


## Report a bug for a Failed Test

- Click on the failed test. It will navigate you to the automation page.
- Click on the bug icon.
- A pop-up menu will appear, fill up the details and create a issue for the same.
- The issue will be notified in the slack channel.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/hyperexecute/integration/products/slack/3.mp4').default} type="video/mp4" />
</video>

## Remove the Slack Integration

- Go to the **Settings** > **Integration** page.
- Select the **Communication** tab and search for Slack.
- Click on the **Remove** button.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/hyperexecute/integration/products/slack/4.mp4').default} type="video/mp4" />
</video>