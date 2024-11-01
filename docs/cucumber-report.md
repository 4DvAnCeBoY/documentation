---
id: cucumber-report
title: Cucumber Report
hide_title: false
sidebar_label: Cucumber
description: Learn how to generate Cucumber Report on lambdatest and download the reports from the dashboard
keywords:
  - cucumber testing reports
  - cucumber testing lambdatest 
url: https://www.lambdatest.com/support/docs/cucumber-report/
site_name: LambdaTest
slug: cucumber-report/
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
          "name": "Cucumber Report",
          "item": "https://www.lambdatest.com/support/docs/cucumber-report/"
        }]
      })
    }}
></script>
Cucumber reporting is a way to visualize and analyze test results when using the Cucumber testing framework. Cucumber is widely used for Behavior-Driven Development (BDD), allowing tests to be written in plain language using Gherkin syntax. The reports generated from Cucumber tests provide a readable format for stakeholders to understand the results, which helps in understanding the behavior of the system being tested without requiring technical expertise.

Cucumber itself provides basic reporting in the command line, but additional plugins and tools can enhance the reporting experience, generating rich HTML or JSON reports.

## Steps to Generate Cucumber Reports on HyperExecute

### Step 1: Configure the TestRunner File
In your `TestRunner` file, configure `@CucumberOptions` to specify report formats and output paths. Here’s an example configuration:

```javascript title="TestRunner.java"
@CucumberOptions(
        features = "src/main/java/Features",
        glue = {"Steps"},
        tags = {"~@Ignore"},
        format = {
                "pretty",
                "html:target/cucumber-reports/cucumber-pretty",
                "json:target/cucumber-reports/CucumberTestReport.json",
                "rerun:target/cucumber-reports/rerun.txt"
        },plugin = "json:target/cucumber-reports/CucumberTestReport.json")
```

Explanation of plugin Options:

- **pretty :** Outputs readable format in console.
- **html:target/cucumber-reports/cucumber-pretty :** Generates HTML report in the target directory.
- **json:target/cucumber-reports/CucumberTestReport.json :** Generates JSON report, often required for CI/CD and advanced reporting.
- **rerun:target/cucumber-reports/rerun.txt :** Logs any failed scenarios for rerun.

### Step 2: Configure the HyperExecute YAML File
In your HyperExecute YAML configuration, define the [`report`](https://www.lambdatest.com/support/docs/deep-dive-into-hyperexecute-yaml/#report) parameters like this:

```yaml title="hyperexecute.yaml"
report: true
partialReports:
 location: target/cucumber-reports/
 frameworkName: cucumber
 type: json
```

### Step 3: Execute Your Tests
Run your tests on HyperExecute using the CLI. After your job completes, you can visit the HyperExecute dashboard to download and view the Cucumber report.

<img loading="lazy" src={require('../assets/images/hyperexecute/knowledge-base/reports/cucumber.png').default} alt="Image" className="doc_img"/> 