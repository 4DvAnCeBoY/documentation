---
id: kaneai-test-manager-access-management
title: Access Management - KaneAI <> Test Manager
hide_title: false
sidebar_label: Access Management - KaneAI <> Test Manager
description: This documentation will help you to understand how to allocate licence to all the users present in your organization
keywords:
- users management lambdatest
- manage user
url: https://www.lambdatest.com/support/docs/kaneai-test-manager-access-management/
site_name: LambdaTest
slug: kaneai-test-manager-access-management/
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
          "name": "Access Management",
          "item": "https://www.lambdatest.com/support/docs/kaneai-test-manager-access-management/"
        }]
      })
    }}
></script>
This document provides guidelines on managing access to KaneAI and Test Manager within LambdaTest. The access management functionality is exclusive to **organization administrators**, allowing them to allocate licenses to users as per the organization's requirements.

## License Allocation Rules
- **License Limitation :** Administrators can only allocate as many licenses as they have purchased or gained licenses through trials.
- **User Addition :** A user can only be added if there is an available license.
- **License Reassignment :** An admin can revoke a license from one user and assign it to another, ensuring optimal resource utilization.
- **Real-Time Monitoring :** Admins can view the current usage of licenses through the Access Management Dashboard.

## Step-by-Step Guide for Managing Access

### Accessing the License Management Panel
**Step 1 :** Log in to your LambdaTest Admin Account. <br />
**Step 2 :** Navigate to **Settings** > **Organization Settings** > **Products**. <br />
**Step 3 :** Select KaneAI or Test Manager tab to allocate the desired product license.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/images/access-management/access-license-panel.mp4').default} type="video/mp4" />
</video>

### Assigning a License to a User
**Step 1 :** Navigate to KaneAI or Test Manager tab for which you want to allocate the license. <br />
**Step 2 :** Click on **Allocate Licenses** button. <br />
**Step 3 :** Select the plan name for which you want to allocate the licenses to your users.<br />
**Step 4 :** Select and add users from your organization to allocate licenses. <br />
**Step 5 :** Click Allocate Licenses to complete the process.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/images/access-management/allocate-licenses.mp4').default} type="video/mp4" />
</video>

### Removing or Reassigning a License
**Step 1 :** Locate the user from the User List. <br />
**Step 2 :** You can select multiple users or for individual users click on the **...** button. <br />
**Step 3 :** Click **Revoke License** to remove access. <br />
> The freed-up license will be available for reassignment. To assign it to another user, follow the [Assigning a License to a User](/support/docs/kaneai-test-manager-access-management/#assigning-a-license-to-a-user) steps.

<video class="right-side" width="100%" controls id="vid">
<source src= {require('../assets/images/access-management/revoke-license.mp4').default} type="video/mp4" />
</video>