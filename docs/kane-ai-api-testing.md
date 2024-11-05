---
id: kane-ai-api-testing
title: KaneAI - API Testing
hide_title: false
sidebar_label: API Testing
description: Learn how to test api via kane ai
keywords:
  - lambdatest automation
  - lambdatest kaneai
  - kaneai scroll elements
  - kaneai sidebar scroll
url: https://www.lambdatest.com/support/docs/kane-ai-api-testing/
site_name: LambdaTest
slug: kane-ai-api-testing/
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
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
          "name": "KaneAI Jira Integration",
          "item": "https://www.lambdatest.com/support/docs/kane-ai-api-testing/"
        }]
      })
    }}
></script>
This document provides a detailed guide to performing API testing using KaneAI. The API testing feature allows for comprehensive backend testing, complementing existing UI testing capabilities. Follow the instructions below to execute API tests using the PetStore API as an example.

## 1. Adding an API in a Web Test

To start API testing on KaneAI, create a web test using the PetStore API, a commonly available sample. This will allow you to demonstrate API testing capabilities effectively.

- **Step**: Add an API through the slash command and navigate to the API module.
  
  <img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/api-testing/image1.jpg').default} alt="kenai-jira integration" className="doc_img"/>
  

## 2. Adding a Curl Command

Within the API module, you can input the curl command to configure the API settings automatically.

- **Step**: Paste your curl command into the designated area. KaneAI will populate all necessary details. You may choose to validate the API response or add it directly to the test steps.

  <img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/api-testing/image2.jpg').default} alt="kenai-jira integration" className="doc_img"/>
  

## 3. Validating API Response on KaneAI

To ensure the API works as expected, use the validation feature. This step confirms that the API responds correctly and can be added to test steps.

- **Step**: Click the 'validate' option to check the API response. A 200 response status indicates successful validation, automatically adding the API to your test steps. You can now proceed to submit multiple APIs simultaneously if needed.

  <img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/api-testing/image3.jpg').default} alt="kenai-jira integration" className="doc_img"/>
  

## 4. Adding Non-Success APIs in Test Steps

For APIs that do not return a 200 status, you can review the response body and manually add them to the test steps as required.

- **Step**: If the API returns a 400 Bad Request or another error, it will not be added automatically. Review the response and add the API manually if needed.

  <img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/api-testing/image8.jpg').default} alt="kenai-jira integration" className="doc_img"/>
  

## 5. Adding Multiple APIs in One Go

KaneAI allows batch processing of multiple APIs to streamline testing. This feature is helpful for scenarios requiring the execution of several API calls in succession.

- **Step**: Add multiple APIs by clicking the plus icon and selecting each API, or paste multiple curl commands to add them automatically to the test steps.

  <img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/api-testing/image10.jpg').default} alt="kenai-jira integration" className="doc_img"/>
  

## 6. Handling Different HTTP Methods

KaneAI supports various HTTP methods like POST, PUT, GET, and DELETE, allowing you to test diverse API interactions.

- **Step**: Add APIs using different HTTP methods, such as a PUT or DELETE command. Validate each API as before, and if successful, they will be automatically included in the test steps.

  
    <img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/api-testing/image6.jpg').default} alt="kenai-jira integration" className="doc_img"/>
  
    <img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/api-testing/image9.jpg').default} alt="kenai-jira integration" className="doc_img"/>

## 7. Executing and Reviewing Test Steps

Once all APIs are added, KaneAI enables simultaneous execution, with details available on methods used, response statuses, and execution times.

- **Step**: Click to execute all added APIs in one go and review the response details for insights into API performance and data returned.

    <img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/api-testing/image13.jpg').default} alt="kenai-jira integration" className="doc_img"/>


This structure provides logical groupings for different aspects of API testing with KaneAI, making it easier to follow each type of action required for comprehensive API testing.