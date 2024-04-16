---
id: analytics-modules-resource-utilization
title: Analytics Modules
sidebar_label: Concurrency Usage Insights
description: Analytics Modules - Resource Utilization
keywords:
  - analytics
url: https://www.lambdatest.com/support/docs/analytics-modules-resource-utilization/
site_name: LambdaTest
slug: analytics-modules-resource-utilization/
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
          "name": "Test Overview",
          "item": "https://www.lambdatest.com/support/docs/analytics-modules-resource-utilization/"
        }]
      })
    }}
></script>

---

# Resource Utilization

The `Resource Utilization` module enables the QA Managers to get an overview of the LambdaTest resources being utilized by their teams.


## About Concurrency Trends

<img loading="lazy" src={require('../assets/images/analytics/resource-utilization-1.png').default} alt="cmd" width="768" height="373" className="doc_img"/>

The Concurrency Trends widget provides a visual representation of your parallel test execution on the LambdaTest platform. It allows you to monitor the number of concurrent sessions running over time, helping you optimize resource utilization and identify peak testing periods.

- X-Axis: Represents the time intervals at which the concurrent sessions are measured.
- Y-Axis: Represents the number of concurrent sessions, categorized into "Queued" and "In Use" sessions.

## How It Works
- The widget tracks the number of concurrent sessions running on the platform over a specified time period.
- It presents the concurrency trends in a graph format, displaying the number of sessions in use and the number of sessions queued at each time interval.
- You can hover over specific data points to view the exact number of sessions in use and queued at that particular time.

## Value Proposition
By analyzing the concurrency trends, you can make informed decisions about scaling your testing infrastructure, ensuring efficient resource allocation, and minimizing queuing times. This widget empowers you to strike the right balance between test execution speed and cost-effectiveness.

:::tip Use case
John is a QA Manager, and his team runs more than 50,000 Jobs in a month across various LambdaTest products like Web Automation, App Automation, and HyperExecute.

John wants to know the duration of the tests kept in queue and the duration of tests put in running state. With the Concurrency Trends widget he can easily track the duration and make a decision to optimize the LambdaTest plan currently subscribed by his team.
:::

<nav aria-label="breadcrumbs">
  <ul className="breadcrumbs">
    <li className="breadcrumbs__item">
      <a className="breadcrumbs__link" target="_self" href="https://www.lambdatest.com">
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
      Resource Utilization 
      </span>
    </li>
  </ul>
</nav>
