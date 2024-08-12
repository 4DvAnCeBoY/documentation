---
id: netlify-integration-with-lambdatest
title: Netlify Integration With LambdaTest
hide_title: true
sidebar_label: Netlify
description: Simplify DevOps! Run blazing-fast Cypress tests on LambdaTest directly from your Netlify builds.
keywords:
  - lambdatest integrations
  - lambdatest netlify integration
  - integrate netlify with lambdatest
  - netlify integration with lambdatest
  - bug tracking tools
  - project management tools
url: https://www.lambdatest.com/support/docs/netlify-integration-with-lambdatest/
site_name: LambdaTest
slug: netlify-integration-with-lambdatest/
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
          "name": "Netlify Integration",
          "item": "https://www.lambdatest.com/support/docs/netlify-integration-with-lambdatest/"
        }]
      })
    }}
></script>

# Netlify Integration with LambdaTest

Netlify is a cloud computing company that offers hosting and serverless backend services for web applications and static websites. It allows developers to deploy their websites and applications quickly and easily, with features such as continuous deployment, serverless functions, and global CDN.

## Prerequisite

1. A LambdaTest account. If you don't have an account, [sign up for free](https://accounts.lambdatest.com/dashboard).

2. You need to have a site deployed in your Netlify account.

## Steps to Setup the Netlify Plugin

### Step 1: Configure your LambdaTest Integration on Netlify Dashboard

- Go to your Netlify Dashboard.

- Click on the Integrations tab, search for **LambdaTest** and click on the **Enable** button.

<img loading="lazy" src={require('../assets/images/netlify-integration/n1.png').default} alt="Image" className="doc_img"/>

- You need to provide your configuration details

    - Enter your **Username** and **Access Key** from the **LambdaTest Dashboard**.

    - Enter your **Smart-UI Project Name**

:::info
For the Smart-UI Project Name, you can enter any project name. Even if you have not set up any projects in the Smart UI Dashboard.

You can also enter your already-existing smart-UI project name.
:::

- Click on the **Save** button

<img loading="lazy" src={require('../assets/images/netlify-integration/n2.png').default} alt="Image" className="doc_img"/>

### Step 2: Deploy the Site for which you want to compare the results

- Go to the **Deploys** section, click on **Deploy site** button and deploy your project. 

<img loading="lazy" src={require('../assets/images/netlify-integration/n3.png').default} alt="Image" className="doc_img"/>

- This deployment is before any changes you have made and will be your **Baseline** image.

- Now you need to make the required changes in your project and push the changes.

- Visit the Netlify Dashboard again, and re-deploy your project.

Your changes will be triggered and deployed.

<img loading="lazy" src={require('../assets/images/netlify-integration/n4.png').default} alt="Image" className="doc_img"/>

### Step 4: Compare the Changes Smart-UI Dashboard

- Go to your Smart-UI Dashbard. You will notice there is already a project with the same name you entered while configuring in **Step 1**

<img loading="lazy" src={require('../assets/images/netlify-integration/n5.png').default} alt="Image" className="doc_img"/>

- Go on that project. Click on the latest build. You can now compare the changes done to your project with-respect-to the provious build.

<img loading="lazy" src={require('../assets/images/netlify-integration/n6.png').default} alt="Image" className="doc_img"/>