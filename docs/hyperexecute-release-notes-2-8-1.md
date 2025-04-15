---
id: hyperexecute-release-notes-2-8-1
title: Version 2.8.1
hide_title: false
sidebar_label: Version 2.8.1
description: Version 2.8.1
keywords:
  - LambdaTest Hyperexecute
  - LambdaTest Hyperexecute help
  - LambdaTest Hyperexecute documentation
  - FAQs
url: https://www.lambdatest.com/support/docs/hyperexecute-release-notes-2-8-1/
site_name: LambdaTest
slug: hyperexecute-release-notes-2-8-1/
---

import NewReleaseTag from '../src/component/newRelease.js';
import EnhancementTag from '../src/component/enhancementTag';
import BugFixTag from '../src/component/bugFixTag';

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
          "name": "Version",
          "item": "https://www.lambdatest.com/support/docs/hyperexecute-release-notes-2-8-1/"
        }]
      })
    }}
></script>
## Enhanced `failFast` at the Scenario Level
We have made am enhancement to our test configuration: the ability to use [`failFast`](http://lambdatest.com/support/docs/deep-dive-into-hyperexecute-yaml/#failfast) at the scenario level!

Previously, `failFast` could only be applied at the test level. Now, with this update, you can configure `failFast` to stop further scenario execution after a specified number of failed scenarios, providing more granular control over your testing process.

### Key Features:
- **Granular Control:** Apply failFast to individual scenarios instead of the entire test suite.
- **Easy Configuration:** Simply set the level to scenario in the YAML configuration.
- **Max Test Failures:** Control the maximum number of allowed test failures at the scenario level.

Example YAML Configuration:

```yaml
failFast:
  maxNumberOfTests: 2
  level: scenario
```

> **Note:** You can use `failFast` either at the test level or scenario level, but not both simultaneously.

This enhancement brings more flexibility to your testing setup, helping you better manage the execution flow and quickly pinpoint issues.