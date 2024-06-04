---
id: smartui-slack-integration
title: Slack Integration with SmartUI
sidebar_label: Slack Integration
description: Effortlessly integrate LambdaTest SmartUI with GitHub App for Visual Regression testing. Follow simple steps to enhance your CI workflow with SmartUI.
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
url: https://www.lambdatest.com/support/docs/ssmartui-slack-integration/
site_name: LambdaTest
slug: smartui-slack-integration/
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
          "name": "WebDriverIO With Appium",
          "item": "https://www.lambdatest.com/support/docs/smartui-slack-integration/"
        }]
      })
    }}
></script>

This document will guide you to integrate your SmartUI jobs and Slack, allowing you to receive real-time notifications and crucial job details directly within your Slack workspace.

## Prerequisite

- An active LambdaTest account with Admin or User-level access. 
- Set up a dedicated Slack channel where you want to receive notifications from SmartUI.
- Should have setup the SmartUI suite.

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

- Go to your desired Project.
- Click on the **Project Settings** button.
- In the **Notifications** tab, toggle the slack alerts to true
- Click on the **Update Settings** button.
- Now again trigger the project with the changes and visit the Slack channel to view the notification containing meta information about the build.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/smart-ui/slack-integration/slack-integration.mp4').default} type="video/mp4" />
</video>

## Remove the Slack Integration

- Go to the **Settings** > **Integration** page.
- Select the **Communication** tab and search for Slack.
- Click on the **Remove** button.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/hyperexecute/integration/products/slack/4.mp4').default} type="video/mp4" />
</video>