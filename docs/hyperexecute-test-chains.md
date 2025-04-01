---
id: hyperexecute-test-chains
title: HyperExecute Test Chains
sidebar_label: Test Chains
description: Discover the power of HyperExecute connected workflows and how testers or developers can leverage it for their daily autoamtion testing of their organization features.
keywords:
  - LambdaTest Hyperexecute
  - LambdaTest Hyperexecute help
  - LambdaTest Hyperexecute documentation
  - LambdaTest Projects
  - Workflows
  - Schedule Workflows
  - Connected Workflows
  - Chained tests
url: https://www.lambdatest.com/support/docs/hyperexecute-test-chains/
site_name: LambdaTest
slug: hyperexecute-test-chains/
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
          "name": "HyperExecute Concepts",
          "item": "https://www.lambdatest.com/support/docs/hyperexecute-test-chains/"
        }]
      })
    }}
></script>
Test Chains allow you to link multiple test workflows so that one workflow triggers another based on specific conditions, such as the success or failure of a previous workflow. This feature eliminates the need for manual intervention between different stages of testing, allowing for a seamless automated testing pipeline.

In this guide, we will walk through the steps to create test chains using connected workflows in HyperExecute, providing real-world examples and step-by-step instructions on how to implement them.

## Features of HyperExecute Connected Workflows
- **Automated Workflow Chains:** Define test chains where the success of one workflow triggers subsequent workflows.
- **Flexible Scheduling:** Schedule workflows to run based on your desired frequency and conditions.
- **Conditional Triggering:** Trigger workflows based on specific outcomes, such as the passing or failing of previous tests.
- **Centralized Configuration:** Set up and manage workflows easily within the HyperExecute platform.

## Real-World Use Case Scenarios
### Example 1: Conditional Regression Testing
Let’s consider a development scenario where:
- **Workflow A** (smoke tests) runs first. This workflow contains a set of critical tests that must pass to ensure the build is functional.
- **Workflow B** (regression tests) runs next, but only if Workflow A passes.

Our objective is to automatically trigger the regression tests after the smoke tests pass to ensure that the software does not break after critical functionalities are verified.

**Workflow Flow:**
- **Workflow A - Smoke tests (runs daily):** Executes a subset of tests (e.g., 30 high-severity or critical tests).
- **Workflow B: Regression tests (triggered after successful execution of Workflow A):** Executes a larger set of tests, ensuring that the product remains functional after code changes.

### Example 2: Severity-based Test Execution
In this scenario, you can define tests to run based on their severity levels.
- **Workflow A:** High-severity tests (e.g., critical functionality tests) are executed every day.
- **Workflow B:** General regression tests (run only after Workflow A passes).

Our objective is to run essential tests first and trigger a broader set of tests only if the critical tests pass.

**Workflow Flow:**
- **Workflow A:** High-severity tests run daily.
- **Workflow B:** General regression tests run if Workflow A passes.

This setup ensures that resources are focused on high-priority tests while the more extensive tests are executed only when necessary.

## Steps to Set Up Connected Workflows in HyperExecute
Follow these steps to configure connected workflows in HyperExecute:

### Prerequisite
- Setup your [Project](/support/docs/hyperexecute-projects/#setup-your-project) before setting up the Workflows.
- You must have created your required [workflows](/support/docs/hyperexecute-projects/#schedule-your-workflows) that you want to trigger.

### Step 1: Setup Workflow
- Click on the "**Setup Workflow**" button:
- Enter Workflow Details:
    - **Workflow Name:** Give your workflow a descriptive name (e.g., "Smoke Tests" or "Regression Tests").
    - **Branch Name:** Specify the branch where your tests are stored.
    - **YAML File Path:** Provide the path to your YAML configuration file that contains the test definitions for this workflow.
- Click "Next" to proceed to the scheduling configuration.

<img loading="lazy" src={require('../assets/images/hyperexecute/knowledge-base/test-chains/1.png').default} alt="Image" className="doc_img"/>

### Step 2: Configure the Schedule
- Configure the schedule of your workflow. Select the **days** and **time** at which you want to trigger your tests. Click on **Next**.

### Step 3: Workflow Linking
You can link this workflow to other existing workflows within the same project or across other projects you own. Once this workflow completes successfully, it can automatically trigger the linked workflows, enabling seamless execution across stages. To set this up, simply select the projects and workflows you wish to trigger from the available list. This feature allows you to build automated, end-to-end workflow chains, ideal for orchestrating complex testing and deployment pipelines.

<img loading="lazy" src={require('../assets/images/hyperexecute/knowledge-base/test-chains/2.png').default} alt="Image" className="doc_img"/>

## Conclusion
HyperExecute’s Test Chain feature significantly enhances the automation of testing processes by creating logical dependencies between workflows. This feature allows for a more efficient, error-free testing pipeline that ensures quality software with minimal manual intervention.

By setting up workflows that automatically trigger based on the outcomes of previous ones, teams can reduce the time spent managing tests, allowing them to focus on critical tasks. Whether you are running smoke tests first, followed by full regression tests, or organizing tests based on severity, HyperExecute provides the flexibility to streamline your testing processes.