---
id: kaneai-upload-and-download-files
title: Upload and Download Files
hide_title: false
sidebar_label: Upload and Download Files
description: This documentation will help you to understand how to Upload and Download Files
keywords:
- upload files
- download files
- kane ai
url: https://www.lambdatest.com/support/docs/kaneai-upload-and-download-files/
site_name: LambdaTest
slug: kaneai-upload-and-download-files/
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
          "name": "Upload and Download Files",
          "item": "https://www.lambdatest.com/support/docs/kaneai-upload-and-download-files/"
        }]
      })
    }}
></script>This guide provides a step-by-step process for uploading and downloading files within Kane AI, a cloud-based testing platform provided by LambdaTest. Users can easily upload files from their local system, access pre-uploaded files, and download files generated during a test session.

## Prerequisites

- A valid LambdaTest account with access to Kane AI.
- An active test session on Kane AI.
- Supported file formats: PNG, B8EF, and CSV.

## Steps to Upload a File
### Step 1: Initiate a Test Session
- Log in to your LambdaTest account.
- Click on **Create a Web Test** to start a new session within Kane AI.

<img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/upload-download-files/image1.png').default} alt="Image" className="doc_img"/>

### Step 2: Navigate to the Upload Section
- Within the test session, navigate to the specific webpage where file uploads are required.
- Type a **`slash (/)`**  to access the file selection menu.

<img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/upload-download-files/image2.png').default} alt="Image" className="doc_img"/>

### Step 3: Select Files for Upload
- Choose to either:
    - Select from pre-uploaded files.
    - Upload files from your local system.
> - Ensure the upload limit does not exceed 5 files per session. <br />
> - Supported formats include PNG, B8EF, and CSV.
- Click **Add File** to confirm your selection.

<img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/upload-download-files/image3.png').default} alt="Image" className="doc_img"/>

### Step 4: File Upload Process
- Upon clicking **Add File**, the selected files are uploaded successfully to the downloads folder within the session.
- These files are treated as variables and their paths are dynamically assigned.

### Step 5: Accessing Uploaded Files
- In the test environment, type upload in the command field.
- Select the required file from the available list using **double-curly braces syntax** (e.g.,`{{IMAGE_ONE}}`).
- Kane AI will detect the appropriate action for uploading and provide relevant options.
- On the right panel, all downloaded files in the session’s downloads folder will be displayed.

<img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/upload-download-files/image4.png').default} alt="Image" className="doc_img"/>

## Downloading Files from Kane AI
### Step 1: Managing Downloaded Files
- Files added during the session will be visible in the downloads section.
- Users can either download all files at once or select specific files for download.

<img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/upload-download-files/image6.png').default} alt="Image" className="doc_img"/>

### Step 2: Reviewing Uploaded Files Post-Test
- After test completion, all uploaded files are recorded as variables.
- These files are also available as attachments in the test summary page for easy reference and download.

The file upload and download functionality in Kane AI enhances test automation by providing easy access to necessary files. By following these steps, testers can efficiently manage files during their test sessions.

<img loading="lazy" src={require('../assets/images/kane-ai/knowledge-base/upload-download-files/image7.png').default} alt="Image" className="doc_img"/>
