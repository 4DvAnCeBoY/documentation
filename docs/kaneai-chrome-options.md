---
id: kaneai-chrome-options
title: Chrome Options
hide_title: false
sidebar_label: Chrome Options
description: This documentation will help you to understand how to use the Chrome Options feature while testing your test cases via KaneAI.
keywords:
  - modules versioning
  - enhancements
  - modules
  - dynamic url
  - chrome options
  - chrome arguments
url: https://www.lambdatest.com/support/docs/kaneai-chrome-options/
site_name: LambdaTest
slug: kaneai-chrome-options/
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
          "name": "Chrome Options",
          "item": "https://www.lambdatest.com/support/docs/kaneai-chrome-options/"
        }]
      })
    }}
></script>
Chrome options, also known as Chrome arguments, are command-line switches that alter the default behavior of the Chrome browser. These options provide flexibility to users by enabling or disabling certain browser features, modifying settings, and configuring custom behaviors such as headless browsing or disabling GPU acceleration.

In KaneAI Web Agent, Chrome options are used to tailor the testing environment to suit the specific needs of automated tests. By defining Chrome options, users can configure the browser behavior before initiating a test session, allowing for a more customized and controlled testing setup. This guide will walk you through the steps to configure and use Chrome options in the KaneAI Web Agent:

## Steps to use Chrome Options in KaneAI Web Agent
Using Chrome options in KaneAI Web Agent is simple and involves defining specific configurations before launching a test. Follow the steps below to add and manage Chrome options for your tests.

### Step 1: Navigate to the Test Configuration Page
- Begin by accessing the Test Configuration page within the KaneAI Web Agent interface. Click on the **Create a Web Test** button.

### Step 2: Locate the Chrome Options Section
- Toggle to On for adding chrome browser command line options to start your instance.
- Enter your Command line switches and you can provide the type of argument as well i.e. String or File for that particular command line.
- You can enter up to 10 Chrome options in the provided input fields.
- For example:
  - `--headless`
  - `--disable-gpu`
  - `--use-file-for-fake-audio-capture=/path/to/audio/file`

<img loading="lazy" src={require('../assets/images/kane-ai/features/chrome-options/1.png').default} alt="Image" className="doc_img"/>

### Step 3: Start the Web Agent
- Once the configuration is done, initiate the Web Agent. The browser will launch with the specified Chrome options applied, allowing you to perform your tests under the customized environment.

## Considerations
- **Maximum Options :** You can configure up to 10 Chrome options per session. Ensure you only input the necessary options for your test case.
- **Supported Options :** KaneAI Web Agent will validate that only supported Chrome options are entered. If you enter an unsupported option, an error message will notify you to correct the configuration.
- **File Paths :** If a Chrome option requires a file path (for instance, `--use-file-for-fake-audio-capture`), KaneAI will automatically inject the Downloads folder path by default. This simplifies the process and removes the need to manually specify file paths for certain features.
- **Default Browser Configuration :** If no Chrome options are provided, KaneAI will default to the standard browser configuration, meaning the browser will launch with its default settings.