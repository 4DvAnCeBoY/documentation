---
id: hyperexecute-release-notes-2-4-8
title: Version 2.4.8
hide_title: false
sidebar_label: Version 2.4.8
description: Version 2.4.8
keywords:
  - LambdaTest Hyperexecute
  - LambdaTest Hyperexecute help
  - LambdaTest Hyperexecute documentation
  - FAQs
url: https://www.lambdatest.com/support/docs/hyperexecute-release-notes-2-4-8/
site_name: LambdaTest
slug: hyperexecute-release-notes-2-4-8/
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
          "name": "Version",
          "item": "https://www.lambdatest.com/support/docs/hyperexecute-release-notes-2-4-7/"
        }]
      })
    }}
></script>

## HyperExecute: Set Dynamic Email Address for Report Sharing 
HyperExecute CLI added an enhancement in the [`--vars`](/support/docs/hyperexecute-cli-run-tests-on-hyperexecute-grid/#--vars) flag providing greater flexibility in specifying email addresses for report and artifact sharing. You can now use a variable to dynamically set the email address used to share reports or artifacts. This gives you more flexibility than hardcoding the email address in the YAML configuration file.

```yaml title="hyperexecute.yaml"
partialReports:
  location: target/surefire-reports/html
  type: html
  frameworkName: extent
  # highlight-start
  email:
      to:
        - "${email}"
        - "${email1}"
  # highlight-end
```

Pass the value of your email address via CLI by running the command

```bash
./hyperexecute --vars "email=xyz@abc.com" --vars "email1=abc@xyz.com"
```

> 📕 Read the documentation - [How to dynamically set your email address?](/support/docs/hyperexecute-email-reports/#how-to-dynamically-set-your-email-address) to learn more about it.