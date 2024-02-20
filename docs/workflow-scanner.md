---
id: workflow-scanner
title: Workflow Scanner
hide_title: false
sidebar_label: Workflow Scanner
description: Workflow Scanner
keywords:
    - LambdaTest
    - Accessibility
    - Testing
    - Workflow Scanner
url: https://www.lambdatest.com/support/docs/workflow-scanner/
site_name: LambdaTest
slug: workflow-scanner/
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
          "name": "How to run Workflow Scanner",
          "item": "https://www.lambdatest.com/support/docs/workflow-scanner/"
        }]
      })
    }}
></script>

Workflow Scan allows you to record multiple real-time interactions and page loads within a user journey on a website and then analyze them for accessibility issues. This helps ensure that users with disabilities can easily navigate and interact with your website across different scenarios.

## Functionalities of Workflow Scan:

- **Identify real-world accessibility issues :** Goes beyond static page analysis and identifies problems users might encounter during interaction.
- **Test complex user flows :** Ensures accessibility throughout navigation, forms, and interactive elements.
- **Save time and effort :** Tests multiple pages at once without needing individual scans.
- **Prioritize issues based on usage :** Focuses on problems encountered in typical user journeys.

## Execute the Full Page Scanner for Your Website

### Prerequisite

- You have to [setup the Accessibility DevTools](/support/docs/accessibility-testing/#how-to-setup-the-accessibility-devtools) in your browser.

### Configure the Accessibility DevTool

- Go to the **Inspect** panel >> **Accessibility DevTools** of your required website.

- Click on the **Workflow Scan** button to start the scanning for **Accessibility Issue** for that particular page.

<img loading="lazy" src={require('../assets/images/accessibility-testing/workflow-scanner/1.png').default} alt="automation-dashboard" className="doc_img"/>

### Review Your Issues

- This will list down all of the issues after scanning all of your webpages that you have searched for.

<img loading="lazy" src={require('../assets/images/accessibility-testing/workflow-scanner/2.png').default} alt="automation-dashboard" className="doc_img"/>