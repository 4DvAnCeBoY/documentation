---
id: accessibility-testing-run-quick-scan
title: Run Your Quick Scan
hide_title: false
sidebar_label: Run Your Quick Scan
description: LambdaTest Run a Quick Scan Accessibility Testing
keywords:
    - LambdaTest
    - Accessibility
    - Testing
    - DevTools
    - run quick scan
    - test issues
url: https://www.lambdatest.com/support/docs/accessibility-testing-run-quick-scan/
site_name: LambdaTest
slug: accessibility-testing-run-quick-scan/
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
          "name": "What is Accessibility Testing",
          "item": "https://www.lambdatest.com/support/docs/accessibility-testing-run-quick-scan/"
        }]
      })
    }}
></script>

### Prerequisite

- You have to [setup the Accessibility DevTools](/support/docs/accessibility-testing-install-devtools) in your browser.

### Trigger the Accessibility DevTool

- Go to the **Inspect** panel >> **LambdaTest Accessibility DevTools** of your required website.
- Click on the **Full Page Scan** button to start the scanning for **Accessibility Issue** for that particular page.

<img loading="lazy" src={require('../assets/images/accessibility-testing/full-page-scanner/1.png').default} alt="automation-dashboard" className="doc_img"/>

### Review Your Issues

- This will list down all of the issues after scanning your complete webpage.
- You can click on those issues to check with which particular element it is causing issue.

<img loading="lazy" src={require('../assets/images/accessibility-testing/full-page-scanner/2.png').default} alt="automation-dashboard" className="doc_img"/>
