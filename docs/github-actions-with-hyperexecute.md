---
id: github-actions-with-hyperexecute
title: GitHub Actions Integration
hide_title: true
sidebar_label: GitHub Actions
description: LambdaTest now integrates with GitHub Actions Pipeline to boost your go-to market delivery. Perform automated cross browser testing with LambdaTest to ensure your development code renders seamlessly through an online Selenium grid providing 3000+ real browsers running through machines.
keywords:
  - lambdatest integrations
  - lambdatest integrations with ci/cd tools
  - ci/cd tools
  - continuous integration,continuous delivery
  - continuous integration tools
  - gitlab ci
url: https://www.lambdatest.com/support/docs/github-actions-with-hyperexecute/
site_name: LambdaTest
slug: github-actions-with-hyperexecute/
---

<script type="application/ld+json"
      dangerouslySetInnerHTML={{ __html: JSON.stringify({
       "@context": "https://schema.org",
        "@type": "BreadcrumbList",
        "itemListElement": [{
          "@type": "ListItem",
          "position": 1,
          "name": "LambdaTest",
          "item": "https://www.lambdatest.com"
        },{
          "@type": "ListItem",
          "position": 2,
          "name": "Support",
          "item": "https://www.lambdatest.com/support/docs/"
        },{
          "@type": "ListItem",
          "position": 3,
          "name": "GitHub Actions Pipeline Integration",
          "item": "https://www.lambdatest.com/support/docs/github-actions-with-hyperexecute/"
        }]
      })
    }}
></script>

# GitHub Actions Pipeline Integration with Hyperexecute
* * *

GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that allows you to automate your build, test, and deployment pipeline. You can create workflows that build and test every pull request to your repository, or deploy merged pull requests to production.

This document will show you how to integrate GitHub Actions Pipeline with HyperExecute to greatly shorten your test cycles.

## How To Integrate GitHub Actions Pipeline with Hyperexecute

***

To integrate GitHub Actions Pipeline with HyperExecute, follow the below steps: 

You can use your own project to configure and test it. For demo purposes, we are using the sample repository.

:::tip Sample repo
Download or Clone the code sample from the LambdaTest GitHub repository to run the tests on the HyperExecute.

<a href="https://github.com/LambdaTest/hyp-ci-cd-integration-sample/tree/main" className="github__anchor"><img loading="lazy" src={require('../assets/images/icons/github.png').default} alt="Image" className="doc_img"/> View on GitHub</a>
:::

### 1. Log into your GitHub account
-  Navigate to the main page of the repository.
-  Under your repository name, click  **Actions**.

### 2. Create a New Workflow
In the left sidebar, click the **New workflow** button. 
 
<img loading="lazy" src={require('../assets/images/hyperexecute/integration/ci-cd/github/github_new_workflow.png').default} alt="Create New Project" width="" height=""/>

### 3. Create the GitHub Actions work-flow YAML file:

To create the GitHub Actions pipeline YAML file, follow the sample command below:

```bash
name: HyperExecute
on:
  workflow_dispatch:
    inputs:
      username:
        required: true
        description: LT Username
      accessKey:
        description: LT Access Key
        required: true
        
jobs:
  HyperExecute:
    runs-on: ubuntu-latest
    timeout-minutes: 15
    strategy:
      fail-fast: false
    steps:
      - name: Checkout sources
        uses: actions/checkout@v2

      - name: Download CLI and Setting Environment Variables
        shell: bash
        run: |
          curl https://downloads.lambdatest.com/hyperexecute/linux/hyperexecute -o hyperexecute
          chmod +x hyperexecute
      
      - name: Executing the Job
        shell: bash
        run: |
          ./hyperexecute --user ${{ github.event.inputs.username }} --key ${{ github.event.inputs.accessKey }} --download-artifacts --config yaml/autosplit_linux.yaml
          echo "Test completion"
```
- **On:**
  - **Workflow_dispatch:** In the **workflow_dispatch** section, you should declare the pre-defined variables that will be used before running the GitHub Actions PipeLine as an input. 
- **Jobs:**
 In the Jobs Section, declare the workflow of the pipeline execution. 
  - **runs-on**: Runs-on contains the value of the OS flavor you would like to execute the GitHub Actions Pipeline on.
- **Steps**:
In the steps section, you should declare the execution commands.  
  - The first step in the above sample YAML changes the path of the root directory.
  - In the second step it downloads the HyperExecute CLI binary. 
  - The third step is the execution command which executes The Hyperexecute CLI binary. This contains LambdaTest username, access key, and path of the Yaml created for Hyperexecute. You can find more information on this [here.](https://www.lambdatest.com/support/docs/hyperexecute-cli-run-tests-on-hyperexecute-grid/)



<img loading="lazy" src={require('../assets/images/hyperexecute/integration/ci-cd/github/github_action_yaml.png').default} alt="Create New Pipeline" width="" height=""/>

### 4. Run the Workflow
To run the new pipeline that you just created, click the **Run workflow** button on the workflow page.
<img loading="lazy" src={require('../assets/images/hyperexecute/integration/ci-cd/github/run_workflow.png').default} alt="Create New Project" width="" height=""/>

<p></p>

**Below is an example of how a test that is run on the GitHub Actions pipeline gets executed:**
<img loading="lazy" src={require('../assets/images/hyperexecute/integration/ci-cd/github/githubactions_example.png').default} alt="Create New Project" width="" height=""/>

<p></p>

**Below is an example of a Hyperexecute job that was triggered through the above pipeline:**
<img loading="lazy" src={require('../assets/images/hyperexecute/integration/ci-cd/github/githubactions_execution.png').default} alt="Create New Project" width="" height=""/>

>
**Run your tests at speeds never seen before. Happy testing! :)**

<nav aria-label="breadcrumbs">
  <ul className="breadcrumbs">
    <li className="breadcrumbs__item">
      <a className="breadcrumbs__link" href="https://www.lambdatest.com">
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
        GitHub Integration
      </span>
    </li>
  </ul>
</nav>