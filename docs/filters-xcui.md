---
id: filters-xcui
title: Filters for XCUI Tests
sidebar_label: Filters for XCUI Tests
description: This document helps you learn how to speed up your XCUI Tests.
keywords:
  - XCUI test filters
  - app test automation
  - XCUI
  - filter
  - lambdatest
  - framework on lambdatest
  - testing in XCUI
  - XCUI testing
  - real devices
url: https://www.lambdatest.com/support/docs/speedup-xcui/
site_name: LambdaTest
slug: speedup-xcui/
---

import CodeBlock from '@theme/CodeBlock';
import {YOUR_LAMBDATEST_USERNAME, YOUR_LAMBDATEST_ACCESS_KEY} from "@site/src/component/keys";

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

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
          "name": "Filters for XCUI Test",
          "item": "https://www.lambdatest.com/support/docs/speedup-xcui/"
        }]
      })
    }}
></script>

Usually, all the test cases of your XCUI test suite are executed, but there is a way to filter these. You can specify some selected classes or tests, which provides you with options to filter the test cases which you want to execute.

To filter the test cases, you just need to pass the suitable parameters in LambdaTest’s REST API request. Refer to the table below to understand how to use various filters provided by LambdaTest.

Given below is the REST API endpoint:

```bash
curl --location --request POST 'https://mobile-api.lambdatest.com/framework/v1/xcui/build' \
--header 'Authorization: Basic BASIC_AUTH_TOKEN' \
--header 'Content-Type: application/json' \
--data-raw '{
  "app" : "APP_ID",
  "testSuite": "TEST_SUITE_ID",
  "device" :  ["iPhone 11-14"],
  "video" : true,
  "queueTimeout": 10800,
  "idleTimeout": 150,
  "devicelog": true,
  "network": false,
  "build" : "Proverbial-XCUITest"
}'
```

| Parameters | Description | Values | Datatype | 
|----------- | ----------- | ------ | -------- |
| `only-testing` | Allows the user to run only those tests/classes provided in the list | Values can be of the following format: className or className/testName. E.g. `["Class1/Test1", "Class2"]` | Array |
| `skip-testing`| Allows the user to run all the tests/classes except the ones provided in the list | Values can be of the following format: className or className/testName. E.g. `["Class1/Test1", "Class2"]` | Array |

:::info Note
You can not use the following filters simultaneously. 
- `only-testing` and `skip-testing`
- `xctestplan` and `only-testing`/`skip-testing`
:::
