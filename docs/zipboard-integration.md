---
id: zipboard-integration
title: zipBoard Integration
hide_title: false
sidebar_label: zipBoard 
description: This document will help you integrate LambdaTest with zipBoard. That way, you can log bugs to your zipBoard project in a single click as you perform cross browser testing with LambdaTest.
keywords:
  - lambdatest integrations
  - push issues to zipboard
  - check browser compatibility online
  - lambdatest zipboard integration
  - cross browser testing tool
  - zipboard integration with lambdatest
  - create zipboard issues from lambdatest
  - bug tracking tools
  - project management tools
url: https://www.lambdatest.com/support/docs/zipboard-integration/
site_name: LambdaTest
slug: zipboard-integration/
---

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
          "name": "Zipboard Integration",
          "item": "https://www.lambdatest.com/support/docs/zipboard-integration/"
        }]
      })
    }}
></script>
ZipBoard is a visual feedback and bug tracking tool designed to streamline collaboration across teams during the web development process. By integrating LambdaTest with ZipBoard, teams can enhance their testing workflows, enabling seamless communication between developers, testers, and stakeholders.

This integration allows you to capture real-time feedback and track issues directly within your test environments on LambdaTest’s cloud platform, ensuring faster bug resolution and better product quality. In this documentation, we’ll guide you through the steps to integrate ZipBoard with LambdaTest and optimize your test management workflow.

## Integrate zipBoard from your LambdaTest Account

**Step 1:** Login to your LambdaTest account. You should have Admin or User level access to see and install integrations.

**Step 2:** Click on Settings -> Integrations -> Bug Tracker.

**Step 3:** Click on **Connect** button of zipBoard block.

**Step 4:** Now, provide your zipBoard API Token to establish integration with LambdaTest and click on **install** button.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/integration/bug-tracking/zipboard/zipboard-integration.mp4').default} type="video/mp4" />
</video>

:::info Fetch your Bugherd API Token
- Visit your zipBoard account -> **Edit Profile** tab.
- Click on the **+** icon to generate your API. Copy your API token to use it for authenticate it with LambdaTest integration.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/integration/bug-tracking/zipboard/zipbaord-api-token.mp4').default} type="video/mp4" />
</video>
:::

> This API key will be used to authenticate your zipBoard account to third-party apps. Please do not share it with anyone. If you believe your API key has been misplaced, you can always generate a new API key from zipBoard by clicking on the refresh icon in your profile settings.

## Lodge your First Bug

**Step 1:** Create a new projects on zipBoard if you haven't already.

**Step 2:** Now, while testing your webapp or application at LambdaTest, click on the **mark as bug** button if you detect any bug.

**Step 3:** Now update the comments of the bug and other details and click on Create Task button.

**Step 4:** Go to your dashboard and check a ticket will be created for the same.

## Uninstall zipBoard Integration

**Step 1:** Login to your LambdaTest account. You should have Admin or User level access to see and install integrations.

**Step 2:** Click on Settings -> Integrations -> Bug Tracker.

**Step 3:** Click on the Remove button.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/videos/integration/bug-tracking/zipboard/remove-zipboard.mp4').default} type="video/mp4" />
</video>

> That was all you need to know for LambdaTest + zipBoard Integration. Increase your productivity with our integrations. If you still have any questions for us, please feel free to let us know. Our experts are always available on <span className="doc__lt" onClick={() => window.openLTChatWidget()}>**chat**</span> to help you out with any roadblock regarding our product. Happy testing! 🙂

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
        Zipboard Integration
      </span>
    </li>
  </ul>
</nav>