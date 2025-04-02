---
id: hyperexecute-release-notes-2-7-8
title: Version 2.7.8
hide_title: false
sidebar_label: Version 2.7.8
description: Version 2.7.8
keywords:
  - LambdaTest Hyperexecute
  - LambdaTest Hyperexecute help
  - LambdaTest Hyperexecute documentation
  - FAQs
url: https://www.lambdatest.com/support/docs/hyperexecute-release-notes-2-7-8/
site_name: LambdaTest
slug: hyperexecute-release-notes-2-7-8/
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
          "item": "https://www.lambdatest.com/support/docs/hyperexecute-release-notes-2-7-8/"
        }]
      })
    }}
></script>
## Default Reporter Configuration in CypressOps
You can now explicitly specify a custom reporter setup using the new `reporterConfigFile` option in [`cypressOps`](https://www.lambdatest.com/support/docs/deep-dive-into-hyperexecute-yaml/#cypressops). If your Cypress project does not have a custom reporter configured, `cypressOps` will automatically enable command logs using the mochawesome reporter by default. This ensures that test results are always captured in a readable format, without requiring manual setup.

```yaml
cypressOps:
  reporterConfigFile: "reporter_config.json"
```

Value of this JSON:

```json
{
  "reporterEnabled": "mochawesome,mocha-junit-reporter",
  "mochawesomeReporterOptions": {
      "reportDir": "cypress/results",
      "overwrite": true,
      "html": false,
      "json": true
  },
  "mochaJunitReporterReporterOptions": {
        "mochaFile": "cypress/results/my-test-output.xml",
        "toConsole": true
  }
}
```

## Setup Runtime Updates
HyperExecute expands its support for the dotnet by introducing the versions `4.7` and `4.8` in the [runtime](https://www.lambdatest.com/support/docs/deep-dive-into-hyperexecute-yaml/#runtime).

```yaml
runtime:
  - language: dotnet
    version: "4.7"
```

## Support for Project Capability in CypressOps
You can now define your [Project](https://www.lambdatest.com/support/docs/hyperexecute-projects/) name and autocreate your project via `ProjectName` capability defined in [`cypressOps`](https://www.lambdatest.com/support/docs/deep-dive-into-hyperexecute-yaml/#cypressops).

```yaml
cypressOps:
  ProjectName: "Cypress_Project"
```

## Consolidated Native Robot Report Generation
The consolidated Native Robot report includes detailed information on all executed tests, i.e., which tests passed, failed, or were skipped, along with any error messages and stack traces for failed tests. It is widely supported across CI/CD tools, which makes it easy to integrate with existing workflows and with other tools or systems.

Add the following configurations in your YAML file:

```yaml
testRunnerCommand: YOUR_RUNNER_COMMAND --outputdir Reports 

report: true
partialReports:
  type: json
  location: Reports
  frameworkName: robot
```

<img loading="lazy" src={require('../assets/images/hyperexecute/release-notes/robot-report.png').default} alt="Image"  className="doc_img"/>