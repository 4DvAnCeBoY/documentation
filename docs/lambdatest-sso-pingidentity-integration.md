---
id: lambdatest-sso-pingidentity-integration
title: LambdaTest SSO & PingIdentity Integration
hide_title: false
sidebar_label: PingIdentity
description: Integrate LambdaTest with Ping Identity for secure SSO using SAML. Follow step-by-step instructions to configure SP-initiated, IdP-initiated SSO, and group management.
keywords:
  - sso
  - lambdatest sso
  - pingidentity
  - lambdatest pingidentity integration
  - lambdatest pingidentity sso
url: https://www.lambdatest.com/support/docs/lambdatest-sso-pingidentity-integration
site_name: LambdaTest
slug: lambdatest-sso-pingidentity-integration/
---

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
          "name": "LambdaTest SSO",
          "item": "https://www.lambdatest.com/support/docs/lambdatest-sso-pingidentity-integration"
        }]
      })
    }}
></script>
LambdaTest provides seamless integration with Ping Identity through SAML (Security Assertion Markup Language) to enable Single Sign-On (SSO) for your organization. By integrating Ping Identity with your LambdaTest organization, you can streamline user authentication and enhance security.

## Key Features of Ping Identity Integration:
- **SP-Initiated SSO :** Single Sign-On initiated from the LambdaTest platform.
- **IdP-Initiated SSO :** Single Sign-On initiated from Ping Identity.

## Prerequisites
Before configuring the integration, ensure you meet the following requirements:

- **LambdaTest Enterprise Plan :** Your organization must have an active Enterprise plan.
- **SSO Enablement Request :** The admin of your LambdaTest organization must request SSO enablement.
> Raise a request via email at support@lambdatest.com or through LambdaTest’s 24/7 in-app chat support.
- **Ping Identity Admin Access :** You need administrative access to your Ping Identity account.

## Configuring LambdaTest & Ping Identity Integration
Follow the steps below to configure the SAML-based integration between LambdaTest and Ping Identity.

### Step 1: Log in to Ping Identity
Log in to your Ping Identity account using admin credentials.

<img loading="lazy" src={require('../assets/images/sso/ping-identity/1.png').default} alt="setup sso button" className="doc_img"/>

### Step 2: Setup SSO in LambdaTest

- Go to LambdaTest <a href="https://accounts.lambdatest.com/auth/sso">Authentication & SSO settings</a> and click on **Setup SSO**.
   <img loading="lazy" src={require('../assets/images/sso-self-serve/setup-sso.png').default} alt="setup sso button" width="944" height="409" className="doc_img"/>

- Enter Connection Name and Click on  **Add New Connection**.
   <img loading="lazy" src={require('../assets/images/sso-self-serve/connection-name.png').default} alt="connection name button" width="944" height="409" className="doc_img"/>

- Select **PingFederate** as your identity provider (PingIdentity & PingFederate has identical setup from LambdaTest side).
   <img loading="lazy" src={require('../assets/images/sso/ping-identity/select-ping.png').default} alt="select identity provider" width="944" height="407" className="doc_img"/>

### Step 3: Add a New Application in PingIdentity
- Navigate to the Applications menu on the toolbar.
- Click on Add Application.
  <img loading="lazy" src={require('../assets/images/sso/ping-identity/2.png').default} alt="add application" className="doc_img"/>

- In the Add Application window, select Create New App to create a new application for LambdaTest SSO integration.
  <img loading="lazy" src={require('../assets/images/sso/ping-identity/3.png').default} alt="create new app" className="doc_img"/>

### Step 4: Add SAML configuration
- In LambdaTest SSO setup copy the **ACS URLs** and **Entity ID**.
  <img loading="lazy" src={require('../assets/images/sso/ping-identity/sso-setup.png').default} alt="ping-integration-sso-setup" width="944" height="487" className="doc_img"/>

- In Pingidentity, select the **Manually Enter** option in **SAML Configuration** and enter **ACS URLs** and **Entity ID** copied from above step.
  <img loading="lazy" src={require('../assets/images/sso/ping-identity/4.png').default} alt="setup sso button" className="doc_img"/>

### Step 5: Configure Attribute Mappings
- Copy following attribute from Lambdatest SSO setup.
   <img loading="lazy" src={require('../assets/images/sso/ping-identity/sso-attribute.png').default} alt="ping-integration-attribute-mapping" width="944" height="487" className="doc_img"/>
- Go to the Attribute Mappings tab of the created application in PingIdentity.
- Update the saml_object attribute value from user_ID to emailaddress.
- Add and update the other attributes
  <img loading="lazy" src={require('../assets/images/sso/ping-identity/6.png').default} alt="attribute-mapping" className="doc_img"/>

### Step 6 : Upload Metadata URL & SSO Domain
- SSO Domains (Comma-separated list of the domains that can be authenticated in the Identity Provider.)
- Copy the **IDP Metadata URL** from PingIdentity
  <img loading="lazy" src={require('../assets/images/sso/ping-identity/7.png').default} alt="ping-integration-idp-url" width="944" height="487" className="doc_img"/>

- Go back to LambdaTest and paste the copied URL in the **Issuer URL** field and click on **Create Connection**:
  <img loading="lazy" src={require('../assets/images/sso/ping-identity/issuer-url.png').default} alt="sso-self serve" width="945" height="542" className="doc_img"/>

After completing these configurations, your LambdaTest and Ping Identity integration for SSO will be ready to use. Both SP-initiated and IdP-initiated SSO flows will be enabled, and you can manage users and groups via Ping Identity.