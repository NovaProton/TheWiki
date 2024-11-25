# Bug Reporting Guide

This guide outlines how to create an effective bug report using GitHub for bug tracking. A well-crafted bug report makes it easier for developers to quickly understand and resolve the issue, improving the quality of our projects.

## Elements of an Effective Bug Report

A good bug report should answer the following questions:

- **What is the problem?**
- **How can the developer reproduce the problem (to see it for themselves)?**
- **Where in the software (which webpage or feature) has the problem appeared?**
- **What is the environment (browser, device, OS) in which the problem has occurred?**

## Components of a Bug Report
An effective bug report should answer questions like: 'What is the problem?', 'How can the developer reproduce it?', 'Where in the software has the problem occurred?', and 'What is the environment in which the issue occurred?'


An effective bug report should contain the following components:

### 1. Title/Bug ID
The title should provide a quick description of the bug. For example, "Distorted Text in FAQ section on homepage". Assigning an ID to the bug also helps with identification.

### 2. Environment
Specify the environment in which the bug appears. The environment can include:
- **Device Type**: Hardware and specific device model
- **OS**: Operating system name and version
- **Tester**: Name of the tester who identified the bug
- **Software Version**: The version of the software being tested
- **Connection Strength**: If the bug is dependent on the internet connection (4G, 3G, WiFi), mention it
- **Rate of Reproduction**: The number of times the bug has been reproduced

### 3. Steps to Reproduce a Bug
Provide a numbered list of steps that lead to the issue. This allows developers to reproduce the bug easily without ambiguity.
Number the steps clearly from first to last so that developers can exactly follow them to see the bug for themselves.

### 4. Expected Result
Describe how the software should behave in the given scenario.

### 5. Actual Result
Detail what the bug is actually doing and how it deviates from the expected result. Be specific:
- Is the software crashing?
- Is it unresponsive?
- Does an error appear?

### 6. Visual Proof of Bug
Screenshots, videos, or logs should be attached to depict the bug clearly. Depending on the nature of the bug, a developer may need different types of proof.

### 7. Bug Severity and Priority
Every bug must be assigned a level of severity and priority.
- **Severity Levels**:
  - **Low**: No noticeable breakdown of the system
  - **Minor**: Unexpected behavior, but system still functions
  - **Major**: Affects large parts of the system
  - **Critical**: Capable of triggering a complete system shutdown
- **Priority Levels**:
  - **Low**: Can be fixed later
  - **Medium**: Regular development priority
  - **High**: Requires immediate attention

## How to Write an Effective Bug Report
You may also use the following template for reporting bugs in GitHub to maintain a consistent and complete report structure.

```markdown
**Title**: [Provide a brief, descriptive title]

**Description**: [Short description of the issue]

**Steps to Reproduce**:
1. Step one
2. Step two

**Expected Result**: [What should happen]

**Actual Result**: [What is happening instead]

**Environment**:
- **Operating System**: [OS details]
- **Browser**: [Browser details]
- **Device**: [Device details]

**Severity**: [Severity level]
**Priority**: [Priority level]

**Attachments**: [Attach screenshots or videos]
```


### Step 1: Craft a Clear and Informative Title
- Be specific and descriptive: "Login Page Error 403 When Accessing via Firefox 115."

### Step 2: Provide a Detailed Summary
- Write a summary that encapsulates the bug's nature and impact. Example: "When attempting to log in using Firefox 115, users encounter a 403 Forbidden error."

### Step 3: List Reproduction Steps
- Detail each step precisely so developers can follow the same process. Example:
  1. Open Firefox 115.
  2. Navigate to the login page.
  3. Enter valid credentials.
  4. Click the "Login" button.

### Step 4: State Expected vs. Actual Results
- **Expected Result**: User should be logged in and redirected to the dashboard.
- **Actual Result**: An error 403 message appears, preventing access.

### Step 5: Describe the Environment
- **Reproducibility**: Indicate whether the bug is 'Always,' 'Often,' or 'Rarely' reproducible.
- Include details like:
  - **Operating System**: Windows 10
  - **Browser**: Firefox 115
  - **Software Version**: 2.1.0

### Step 6: Attach Error Messages and Logs
- Provide relevant information, such as error messages, codes, or logs.

### Step 7: Include Visual Evidence
- Attach screenshots or videos to provide additional context.

### Step 8: Assess Severity and Priority
- Use the following definitions to help classify the severity and priority accurately:
  - **Severity**:
    - **Low**: Minimal impact, no noticeable breakdown.
    - **Minor**: Unexpected behavior but still functional.
    - **Major**: Significant issues affecting functionality.
    - **Critical**: System-wide failure or shutdown.
  - **Priority**:
    - **Low**: Can be deferred.
    - **Medium**: Address during regular development cycles.
    - **High**: Needs immediate resolution.

- Determine the severity and priority:
  - **Severity**: Critical (blocks login)
  - **Priority**: High (requires immediate fix)

### Step 9: Provide Additional Context
- Include any extra information, such as the frequency of the issue or recent changes that may be related.

### Step 10: Confirm Reproducibility
- Indicate if the issue can be consistently reproduced or if it occurs intermittently.

### Step 11: Assign and Follow Up
- Assign the bug report to the relevant developer and follow up to ensure the issue is resolved.

## Best Practices for Creating a Bug Report

### Do’s
- **Be Clear and Specific**: "App crashes when clicking the 'Submit' button."
- **Provide Detailed Steps**: List step-by-step instructions to reproduce.
- **Include Environment Details**: Mention OS, browser version, device type, etc.
- **Use Visuals**: Add screenshots, logs, or videos.
- **Assign Correct Severity and Priority**: Evaluate the impact accurately.

### Don’ts
- **Avoid Vague Descriptions**: "Something is wrong with the login page."
- **Skip Essential Details**: Include steps, environment, and expected behavior.
- **Use Complex Jargon**: Keep it simple for everyone to understand.
- **Include Irrelevant Information**: Focus on the bug, not personal anecdotes.
- **Make Assumptions**: Stick to facts without speculation.

