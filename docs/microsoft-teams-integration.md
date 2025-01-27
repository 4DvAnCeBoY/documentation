---
id: microsoft-teams-integration
title: Microsoft Teams Integration
hide_title: false
sidebar_label: Microsoft Teams
description: LambdaTest integration with Microsoft Teams allows you to push a bug directly to your specified Teams channel from LambdaTest platform. Share your UI observations and input with your teammates on any time, by capturing a screenshot in the middle of your test session through LambdaTest. You can annotate the screenshot & highlight your issue or input. The fields populated by you when marking as a bug through LambdaTest are displayed as information on the respective Teams channel for that testing instance.
keywords:
  - microsoft teams integration
  - lambdatest integration
  - bug reporting
  - team communication
url: https://www.lambdatest.com/support/docs/microsoft-teams-integration/
site_name: LambdaTest
slug: microsoft-teams-integration/
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
          "name": "Microsoft Teams Integration",
          "item": "https://www.lambdatest.com/support/docs/microsoft-teams-integration/"
        }]
      })
    }}
></script>
Microsoft Teams is a leading communication and collaboration platform that combines workplace chat, video conferencing, file storage, and app integration. Designed for teamwork, it enables seamless interaction and productivity within organizations, making it an ideal tool for managing projects and workflows.

The Microsoft Teams integration with LambdaTest enables seamless collaboration and real-time updates on your test automation workflows. With this integration, you can:
- Receive instant notifications on test status and results directly in your Microsoft Teams channels.
- Collaborate efficiently by sharing test execution logs and reports with your team.
- Stay informed about your test runs without leaving your Teams environment.

> **NOTE :** You must have either any **Bug Tracker** or **Project Management** tool integrated before proceeding with Teams integration.

## Generate your Webhook URL

**Step 1:** Visit your Teams account -> click on the **+** button and create a channel in which you want to receive all your notifications.

**Step 2:** Click on the **...** button in the top right section of your channel and select workflows.

**Step 3:** Provide the description and create a new workflow by selecting the channels 

<img loading="lazy" src={require('../assets/images/integrations/microsoft-teams/3.png').default} alt="Image" className="doc_img img_center"/>

**Step 4:** Copy your generated workflow, you will need it in the next step.

<img loading="lazy" src={require('../assets/images/integrations/microsoft-teams/4.png').default} alt="Image" className="doc_img img_center"/>

## Integrate Teams with your LambdaTest Account

**Step 1:** Login to your LambdaTest account. You should have Admin or User level access to see and install integrations.

**Step 2:** Click on Settings -> Integrations -> Communication.

**Step 3:** Click on **Connect** button of `Microsoft Teams` block.

**Step 4:** Now, provide your Microsoft Teams Workflow URL to establish integration with LambdaTest and click on **install** button.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/images/integrations/microsoft-teams/connect-worflow.mp4').default} type="video/mp4" />
</video>

## Lodge your First Bug

> Note: If you are using Rocket.Chat for the first time, then make sure to create a project for yourself. It is a pre-requisite in order to push screenshots from your LambdaTest account.

**Step 1:** Start with any type of testing, for the demo purpose we are going with the **Real Time Testing**.

**Step 2:** Enter your Project URL and configure for browser and operating system of your choice & hit **Start**.

**Step 3:** After the VM is launched and operable. You can perform testing on your web-app for finding bugs. If a bug gets revealed, then you need to click on the Bug icon from the left panel for capturing a screenshot of the same.

**Step 4:** After clicking on "**Mark as Bug**" button your respective **Bug Tracker** tool or **Project Management** tool specific form would open up. Fill the fields as per your requirement.

> Make sure you mark on the check at the last of the form to send the notification on your integrated Teams channel.

**Step 5:** Click on **Mark as Bug** button. Now go to your dashboard and check a ticket will be created for the same.

**Step 6:** Go to your Teams channel and you can check a notification is sent for the same.

## Uninstall Microsoft Teams Integration

**Step 1:** Login to your LambdaTest account. You should have Admin or User level access to see and install integrations.

**Step 2:** Click on Settings -> Integrations -> Communication.

**Step 3:** Click on the **Remove** button.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/images/integrations/microsoft-teams/connect-worflow.mp4').default} type="video/mp4" />
</video>

> That was all you need to know for LambdaTest + Teams Integration. Increase your productivity multifold with our integrations. If you still have any questions for us, please feel free to let us know. Our experts are always <span className="doc__lt" onClick={() => window.openLTChatWidget()}>**available on chat**</span> to help you out with any roadblock regarding our product. Happy testing!