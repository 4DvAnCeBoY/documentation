---
id: analytics-dashboard-settings
title: Analytics Dashboard Settings
sidebar_label: Dashboard Settings
description: Customize your Analytics Dashboard settings for optimal test analysis. Learn how to adjust settings to fit your testing needs.
keywords:
  - analytics
url: https://www.lambdatest.com/support/docs/analytics-dashboard-settings/
site_name: LambdaTest
slug: analytics-dashboard-settings/
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
          "name": "Linear App Integration",
          "item": "https://www.lambdatest.com/support/docs/analytics-dashboard-settings/"
        }]
      })
    }}
></script>

## Dashboard Settings Overview

The Analytics Dashboard Settings page provides a comprehensive set of controls to help you manage notifications, sharing, and access for your test analytics dashboards. This guide details each setting and how to use it for optimal collaboration and visibility.

---

### Email Notification Settings

Keep your team informed about dashboard activity and test results by configuring email notifications.

- **Enable/Disable Notifications:** Use the toggle to activate or deactivate email notifications for the dashboard. When disabled, no email updates will be sent.
- **Notification Frequency:** Choose how often you want to receive email updates. Options typically include Daily, Weekly, or Custom intervals, allowing you to match your team's workflow.
- **Date Range:** Select the default date range or specify a custom number of days to include in each notification. For example, setting a custom range to 7 will include data from the last 7 days in each email.
- **Add Recipients:** Enter one or more email addresses to receive notifications. Click **Add** after each address to include multiple recipients. This is useful for keeping stakeholders, QA leads, or team members in the loop.
- **Update & Save Preferences:** After configuring your preferences, click **Update** to save changes. Your notification settings will take effect immediately.

> **Tip:** Use custom date ranges and recipient lists to tailor notifications for different teams or reporting needs.

---

### Slack Notification Settings

Integrate your dashboard with Slack to receive instant updates and foster real-time collaboration.

- **Enable/Disable Notifications:** Toggle Slack notifications on or off as needed. When enabled, updates will be sent directly to your selected Slack channel.
- **Notification Frequency:** Set how often notifications are sent to Slack (e.g., Daily, Weekly). This helps avoid notification fatigue while ensuring timely updates.
- **Date Range:** Choose the default or set a custom range (number of days) to define the scope of data included in each notification.
- **View Selection:** Select the specific dashboard view or analytics channel for which notifications should be sent. This allows you to target relevant information to the right Slack channels or teams.
- **Update & Save Preferences:** Click **Update** to apply your Slack notification settings.

> **Best Practice:** Use Slack notifications for critical dashboards or to alert teams about important trends, regressions, or test failures.

---

### MS Teams Notification Settings

Integrate your dashboard with Microsoft Teams to receive timely updates and enhance team collaboration.

- **Enable/Disable Notifications:** Toggle MS Teams notifications on or off as needed. When enabled, updates will be sent directly to your selected Teams channel.
- **Notification Frequency:** Set how often notifications are sent to MS Teams (e.g., Daily, Weekly). This helps ensure your team stays informed without overwhelming them with messages.
- **Date Range:** Choose the default or set a custom range (number of days) to define the scope of data included in each notification.
- **View Selection:** Select the specific dashboard view or analytics channel for which notifications should be sent. This allows you to target relevant information to the right Teams channels or groups.
- **Update & Save Preferences:** Click **Update** to apply your MS Teams notification settings.

> **Best Practice:** Use MS Teams notifications for dashboards that require broad visibility or to alert teams about important trends, regressions, or test failures.

---

### Share Link Settings

Easily share your dashboard with colleagues, clients, or external stakeholders while maintaining control over access and privacy.

- **Link Expiration:** Set the share link to expire after 7, 15, or 30 days, or select **Never** for a permanent link. Expiring links are recommended for temporary collaborations or reviews.
- **Privacy Controls:**
  - **Make Dashboard Private:** Restrict access so only you can view the dashboard. Use this for sensitive or in-progress dashboards.
  - **Allow Anyone with the Link:** Enable open access for anyone who has the link, ideal for broad sharing within your organization.
  - **Set a Custom Password:** Add an extra layer of security by requiring users to enter a password to access the dashboard. This is especially useful when sharing with external users or when the link has no expiry.

:::note
Password setup is mandatory if you select "Never" for link expiry. Exporting the dashboard will be disabled in this case to protect sensitive data.
:::

- **Export Restrictions:** If you set the link to never expire and require a password, dashboard export functionality will be disabled to enhance security.

> **Security Tip:** Always use password protection and link expiration when sharing dashboards outside your core team.

---

### Edit Dashboard Name

Personalize your dashboard for clarity and easy identification.

1. Enter a new name in the **Dashboard Name** field at the top of the settings panel. Use descriptive names that reflect the dashboard's purpose (e.g., "SMOKE Dashboard for Prod Playwright").
2. Click **Save** to apply the new name. The updated name will be visible to all users with access to the dashboard.

> **Tip:** Use naming conventions to organize dashboards by project, environment, or team.

---

### Delete the Dashboard

Remove dashboards that are no longer needed to keep your workspace organized and secure.

1. Scroll to the bottom of the settings panel.
2. Click the **Delete** button next to "Delete this Dashboard".
3. Confirm the deletion when prompted.

:::danger
This action is irreversible. Once deleted, the dashboard and all its data cannot be recovered. Ensure you have exported or backed up any important information before proceeding.
:::

> **Recommendation:** Only delete dashboards when you are certain they are no longer required by any team members.

---

### Additional Support

For more information and advanced configuration options, reach out to our support team at [support@lambdatest.com](mailto:support@lambdatest.com).
