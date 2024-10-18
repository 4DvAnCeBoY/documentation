---
id: kane-ai-web-test-writing-guidelines
title: KaneAI Web Agent - Guidelines for Writing Instructions
hide_title: false
sidebar_label: Web Agent Instruction Guide
description: Learn how to write instructions for running the kane ai web agent smoothly and without any problem
keywords:
  - lambdatest automation
  - lambdatest kaneai
  - kaneai Web test
  - kaneai guidelines
  - instructions writings
url: https://www.lambdatest.com/support/docs/kane-ai-web-test-writing-guidelines
site_name: LambdaTest
slug: kane-ai-web-test-writing-guidelines/
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
          "name": "KaneAI Web Test",
          "item": "https://www.lambdatest.com/support/docs/kane-ai-web-test-writing-guidelines"
        }]
      })
    }}
></script>
The KaneAI Web Agent is an automation tool that executes web interactions based on natural language instructions. This guide provides best practices for writing clear, user-friendly instructions when using the KaneAI Web Agent. The goal is to ensure accurate execution of tasks by the AI and improve the quality of interactions with web elements.

## General Instruction

### 1. Clarity and Specificity
Always provide clear and specific instructions for the action you wish to perform. Use the appropriate terminology from the list of supported commands. Avoid vague terms such as `do this` or `click that`—be explicit about which element to interact with.

### 2. Context
When the action is dependent on a specific element or section of a webpage, provide enough context to help identify the element. Example: `Click the 'Submit' button on the top right corner of the form`.

### 3. Step-by-Step Instructions
Break down complex tasks into smaller, manageable steps. Use logical connectors like `then` or `after that` to indicate the sequence of actions. Clearly specify the flow, such as `Click 'Login', then type your email in the input field.`

### 4. Use Examples
Refer to the examples provided in the list of supported commands for guidance on structuring your instructions.
Example: `Type 'username' in the search bar and press 'Enter' to submit.`

### 5. Wait Command
Use the wait command when needed to pause execution, allowing operations or page loads to complete before proceeding to the next action. Example: `Click 'Submit' and wait for 5 seconds before proceeding to the next step.`

### 6. Refining Prompts
If the AI response is not as expected, refine your prompt by adding more details or increasing clarity. Use iterative refinement to achieve the desired outcome.

### 7. Tab Targeting
When interacting with elements that open in a new tab, use the prompt `switch to the <TabTitle> tab` to ensure actions stay on the newly opened tab.

## DO's & DON'Ts

### DO's
- **Specify the Exact Element :** Clearly indicate which element you want to interact with. For instance, use the element's name, position, or attributes.
Example: `Click on the second product in the list.`

- **Use Action Verbs :** Start your instructions with action verbs like "Click," "Type," "Hover," etc.
Example: `Hover over the navigation bar.`

- **Provide Context for Conditional Actions :** If the action depends on an element’s visibility or existence, include this in the instruction. Example: `If the 'Login' button is visible, click it.`

- **Use Numbers to Indicate Positions or Quantities :** When specifying positions or quantities, use numbers for clarity. Example: `Scroll down 100 pixels.`

- **Verify Steps Before Saving Test Cases :** Use the re-run option to ensure KaneAI executes all steps correctly and without errors before saving the test case.

- **Validate Test Flow While Editing :** Let the test run to validate if the flow is correct while editing a test case. Click "Resume" only after all steps are completed.

- **Use Manual Interaction When Necessary :** If KaneAI struggles to execute the desired action, manually intervene to guide the AI appropriately.

### DON'Ts
- **Avoid Vague Terms :** Do not use terms like "Click that" or "Do this" without specifying which element or action.

- **Do Not Assume Context Without Detail :** Ensure instructions are detailed enough for the AI to understand which elements are involved. Example of what to avoid: `Click the button" (without specifying which button)`.

- **Avoid Overloading Instructions :** Do not combine too many actions into a single instruction unless they are logically sequenced. Example of what to avoid: `Click the button and type in the field and then hover.`

- **Do Not Mix Unrelated Commands Without Logical Sequence :** Keep commands logically connected. Avoid mixing different actions without specifying the sequence. Example of what to avoid: `Click and then go to a new tab (without a clear sequence)`.

- **Always Verify Results for Assertions :** When using assertions, confirm that the expected result occurs to ensure success.

- **Acknowledge AI Limitations :** If the AI doesn’t perform the desired action, refine the prompt instead of expecting perfect results on the first try.

- **Use Iterative Approach for Accuracy :** Allow the AI to process, execute the action, and respond. If the initial outcome isn’t correct, refine and reissue the prompt iteratively.

- **Avoid Unnecessary Jargon :** Use simple language to communicate instructions. Only use technical terms when necessary.