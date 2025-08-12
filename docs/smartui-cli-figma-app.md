---
id: smartui-cli-figma-app
title: Getting Started with LambdaTest's SmartUI Figma-App CLI
sidebar_label: Figma-App CLI
description: Learn how to compare your Figma mobile designs with native app screenshots on real devices using SmartUI CLI.
keywords:
  - Visual Regression
  - Mobile App Visual Testing
  - Figma to App Comparison
  - SmartUI CLI
  - LambdaTest Mobile
  - Design to Production Validation
url: https://www.lambdatest.com/support/docs/smartui-cli/
slug: smartui-cli-figma-app/
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import CodeBlock from '@theme/CodeBlock';

---

SmartUI Figma-App CLI lets you compare **mobile app screenshots captured on real devices** with your **Figma design frames** to detect visual mismatches and ensure accurate implementation of mobile UI.

---

## Prerequisites

- Node.js and npm installed
- LambdaTest SmartUI account with App Automation plan
- Real device screenshots captured via Appium, SDK, or SmartUI platform
- Figma Personal Access Token ([how to get one](https://help.figma.com/hc/en-us/articles/8085703771159-Manage-personal-access-tokens))

---

## Understanding Figma Tokens

| Token                | Where It’s Used | Description                                                                 |
|----------------------|------------------|-----------------------------------------------------------------------------|
| `FIGMA_TOKEN`        | Env Variable     | Your Figma **Personal Access Token** to authenticate with the Figma API    |
| `figma_file_token`   | `designs.json`   | Figma **file ID**, extracted from the Figma file URL                       |
| `figma_ids`          | `designs.json`   | List of **frame or node IDs** you want to compare visually                 |

> Example Figma URL:  
> `https://www.figma.com/file/abc12345/file-name?node-id=2417-58969`  
> - `figma_file_token`: `abc12345`  
> - `figma_ids`: `2417-58969`

---

## Step-by-Step Guide

### 1. Create a SmartUI Project

1. Visit [smartui.lambdatest.com](https://smartui.lambdatest.com)
2. Click **New Project**
3. Select **Real Devices** as the platform
4. Enter:
   - Project Name
   - Approvers (optional)
   - Tags (optional)
5. Click **Submit**

---

### 2. Install SmartUI CLI

```bash
npm install @lambdatest/smartui-cli
````

---

### 3. Generate and Edit Configuration

Run the following to create your initial design file:

```bash
npx smartui config:create-figma-app designs.json
```

#### Sample `designs.json`

```json title="designs.json"
{
  "mobile": [
    {
      "name": "Pixel 8",
      "platform": ["Android 14"],
      "orientation": "portrait"
    }
  ],
  "figma": {
    "depth": 2,
    "configs": [
      {
        "figma_file_token": "abc12345",
        "figma_ids": ["2417-58969"],
        "screenshot_names": ["homepage"]
      }
    ]
  }
}
```
---

### 4. Set Environment Variables

```bash
export PROJECT_TOKEN="your_smartui_project_token"
export FIGMA_TOKEN="your_figma_personal_token"
```

---

### 5. Run the Comparison

```bash
npx smartui upload-figma-app designs.json
```

#### Optional Flags

| Flag             | Description                                       |
| ---------------- | ------------------------------------------------- |
| `--markBaseline` | Mark this build as a new baseline for future runs |
| `--buildName`    | Assign a custom name to this comparison build     |

#### Example

```bash
npx smartui upload-figma-app designs.json --buildName "v1.0.0" --markBaseline
```

---

### View SmartUI Results

You can see the Smart UI dashboard to view the results. This will help you identify the Mismatches from the existing `Baseline` build and do the required visual testing.

<img loading="lazy" src={require('../assets/images/smart-visual-testing/smartui-sdk-results-primer.webp').default} alt="cmd" width="768" height="373" className="doc_img"/>

### Additional Resources

* [How to generate a Figma token](https://help.figma.com/hc/en-us/articles/8085703771159-Manage-personal-access-tokens)
* [SmartUI CLI Docs](https://www.lambdatest.com/support/docs/smartui-cli/)
* [Appium + SmartUI Node Sample](https://github.com/LambdaTest/smartui-appium-nodejs)

---

**Run seamless visual comparisons between real device screenshots and Figma designs with SmartUI CLI. Start validating your mobile UI today!**