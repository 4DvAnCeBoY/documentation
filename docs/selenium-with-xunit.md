---
id: selenium-xunit
title: How to Run Selenium Tests With xUnit
hide_title: true
sidebar_label: xUnit
description: Learn how to run your first Selenium test with xUnit on LambdaTest.
keywords:
- selenium xunit
- selenium with xunit
- selenium with xunit on lambdatest
- xunit lambdatest
url: https://www.lambdatest.com/support/docs/selenium-with-xunit/
site_name: LambdaTest
slug: selenium-with-xunit/
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
          "name": "Run Selenium Tests With xUnit on LambdaTest",
          "item": "https://www.lambdatest.com/support/docs/selenium-with-xunit/"
        }]
      })
    }}
></script>

# Run Selenium Tests With xUnit
---

Learn how to run your xUnit automation testing scripts on LambdaTest online Selenium Grid of 3000+ real browsers and operating systems.

## Prerequisites
---

Before you start performing C# automation testing with Selenium using xUnit, you need to:

1. Download and install Selenium WebDriver from its official website.
2. Ensure you have the latest version of C#.
3. .NET framework for guidelines while developing a range of applications using C#.
4. Download Selenium WebDriver Language Binding for C# and extract them to the appropriate folder. 
5. Install a .NET Core SDK of 8.0 or greater version.

## Installing Selenium Dependencies
---

1. Clone the LambdaTest Selenium xUnit GitHub repository and navigate to the code directory:

```
git clone https://github.com/LambdaTest/CSharp-xUnit-Selenium
cd CSharp-xUnit-Selenium
```

## Setting up Your Authentication
---

Ensure you have your LambdaTest credentials to run C# automation scripts. Get these credentials from the LambdaTest Profile by heading to **Account Settings** > **Password & Securit**y tab.

2. Set your LambdaTest Username and Access Key in environment variables.

**Windows**:

```bash
set LT_USERNAME="YOUR_USERNAME"
set LT_ACCESS_KEY="YOUR_ACCESS_KEY"
```

**macOS/Linux**:

```bash
export LT_USERNAME="YOUR_USERNAME" 
export LT_ACCESS_KEY="YOUR_ACCESS_KEY"
```

## Running Your First xUnit Test
---

>**Test Scenario**: Check out the sample *SingleTest.cs* file. This xUnit Selenium script tests a sample to-do list app by marking a couple of items as done, adding a new item to the list, and finally displaying the count of pending items as output.

3. Navigate to *[config.json](https://github.com/LambdaTest/CSharp-xUnit-Selenium/blob/master/XUnit-LambdaTest/config.json/)* using VS Code. Replace this code in the *config.json* file in your project.

## Configuring Test Capabilities
---

4.  In the *config.json* file, update your test capabilities. We are passing browser, browser version, and operating system information, along with LambdaTest Selenium Grid capabilities via the capabilities object.

```csharp
{
  "server": "hub.lambdatest.com",
  "user": "LT_USERNAME",
  "key": "LT_ACCESS_KEY",

  "capabilities": {
    "lt:options": {
      "buildName": "xunit build",
      "sessionName": "lambdatest xunit sample test",
      "visual": "true",
      "plugin": "xunit:sample"
    }
  },

  "environments": [
    {
      "browserName": "chrome"
    },
    {
      "browserName": "firefox"
    },
    {
      "browserName": "safari"
    }
  ],

  "TunnelOptions": {
    "tunnel": false
  }
}
```

## Executing the Test
---

5. Build the solution in Visual Studio.

6. Run the tests from the Test Explorer in Visual Studio.

* If you are using macOS or Linux, to run the tests, clean and rebuild the project using the below command:

```csharp
dotnet clean
```

* Now, run the single test using the below command:

```csharp
dotnet test --filter "profile=single"
```

## Running Your xUnit Tests in Parallel
---

**For Windows**:

To execute parallel tests on Windows, run all tests from the Test Explorer in Visual Studio.

**For macOS/Linux**:

To execute parallel tests on macOS or Linux, run the below command:

```csharp
dotnet test --filter "profile=parallel"
```

## Testing Locally Hosted Or Privately Hosted Web Projects
---

For testing locally hosted or privately hosted projects with LambdaTest Selenium Grid using LambdaTest Tunnel, follow the [LambdaTest Tunnel documentation](https://www.lambdatest.com/support/docs/testing-locally-hosted-pages/).

Download the LambdaTest Tunnel binary for your OS and run the following command:

```csharp
LT -user {user’s login email} -key {user’s access key}
Tunnel Capability
```

**Tunnel Capability**:

```csharp
"lt:options": {
      "buildName": "xunit build",
      "sessionName": "lambdatest xunit sample test",
      "visual": "true",
      "plugin": "xunit:sample",
      "tunnel": "true"
    }
```












