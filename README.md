# Snathak-Scrum-1



# VCS Notification Documentation


| Created/Modified | Version | Author              | Comment         |  Reviewer     |
|-------------------|---------|---------------------|-----------------|-----------------|
| 11-11-2024        | V1      | Pratham Kukudkar | Initial Commit  |                 |
| 15-11-2024        | V2      | Pratham Kukudkar | L0 feedbacks    |                       |



## Table of Contents

- [Introduction](#introduction)
- [Pre-requisites](#pre-requisites)
- [Step-by-Step Setup Guide](#step-by-step-setup-guide)
- [Best Practices](#best-practices-for-setting-up-and-managing-vcs-notifications)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)

---

## Introduction
Version Control Systems (VCS) are essential tools in modern software development, allowing teams to manage changes to source code over time. Notifications in VCS help keep team members informed about changes, updates, and activities within repositories. This document provides a comprehensive guide on setting up and managing VCS notifications effectively.

## Pre-requisites
Before setting up the VCS Notification System, ensure you have the following:

- A version control system (e.g., GitHub, GitLab, Bitbucket) installed and configured.
- Access to a repository on a VCS hosting platform (e.g., GitHub, GitLab, Bitbucket).
- Administrative or sufficient permissions to configure notification settings.
- A communication platform for notifications (e.g., Slack, Microsoft Teams, email) for receiving notifications.
- Basic knowledge of VCS and webhooks.

## Step-by-Step Setup Guide


## 1. Slack Notifications

### Step 1: Create a Slack App

1. **Go to the Slack API**: Navigate to [Slack API](https://api.slack.com/).
2. **Create New App**:
    - Click on "Create New App".
    - Select "From scratch".
    - Name your app.
    - Choose your workspace.

### Step 2: Configure Incoming Webhooks

1. **Navigate to Incoming Webhooks**:
    - In your app settings, find and click on "Incoming Webhooks".
2. **Activate Incoming Webhooks**:
    - Enable Incoming Webhooks.
    - Add a new webhook to your workspace.
3. **Select the Channel**:
    - Choose the channel where notifications will be posted.
    - Authorize the app.
4. **Copy Webhook URL**:
    - Copy the provided webhook URL for use in the next steps.

### Step 3: Set Up GitHub Integration

1. **Go to GitHub Repository**:
    - Open your GitHub repository.
2. **Navigate to Webhooks**:
    - Click on "Settings".
    - Click on ["Webhooks"](https://github.com/MyGurukulam-p11/Documentation-P11/settings/hooks).
3. **Add New Webhook**:
    - Paste the Slack webhook URL into the "Payload URL" field.
    - Set "Content type" to `application/json`.
    - Choose the events (e.g., pushes, pull requests) that should trigger notifications.
    - Save your webhook.

## 2. Email Notifications

### Step 1: GitHub's Notification Settings

1. **Navigate to Notification Settings**:
    - Go to GitHub's notification settings.
2. **Ensure Email is Correct**:
    - Verify that your email address is correct.
3. **Select Activities**:
    - Choose which activities (e.g., comments, pushes) you want to receive emails about.
4. **Customize Preferences**:
    - Adjust your notification preferences as needed.

### Step 2: Custom Email Notifications (Optional)

1. **Create a GitHub Actions Workflow**:
    - Go to your repository and click on "Actions".
    - Create a new workflow or choose a template.
2. **Use YAML File for Custom Notifications**:
    - Use the provided YAML file (e.g., `notify.yml`) to send custom email notifications.
3. **Add Email Credentials**:
    - Add your email credentials as secrets in your repository settings under "Actions".

  
## Best Practices for Setting Up and Managing VCS Notifications

| Best Practice            | Purpose                                                                       | Action                                                                                      |
|--------------------------|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Regular Testing          | Ensure notifications work correctly.                                            | Regularly test by making commits or pull requests to verify notifications.                   |
| Security                 | Protect sensitive information (e.g., webhook URLs, email credentials).          | Securely store credentials as secrets and limit access to trusted personnel.                  |
| Customization            | Tailor notifications to team needs.                                              | Customize settings to deliver relevant information without unnecessary noise.                |
| Selective Notifications  | Avoid overload by focusing on important events.                                  | Enable notifications only for critical activities like major changes or urgent issues.        |
| Structured Messages      | Ensure notifications are clear and informative.                                 | Format messages with essential details like commit messages, authors, and branches.          |
| Monitor and Adjust       | Improve notification effectiveness over time.                                   | Regularly review settings based on team feedback and adjust for better communication flow.    |



## Conclusion
Setting up a VCS Notification System enhances team collaboration and keeps everyone informed of important changes in the codebase. By following the steps outlined in this guide and adhering to best practices, you can ensure a smooth and efficient notification system that supports your development workflow.

## Contact Information

| Name          | Email address           |
|---------------|-------------------------|
| Pratham Kukudkar | pratham.kukudkar.snaatak@mygurukulam.co |

## References

| Reference                                                               | Name                       |
|-------------------------------------------------------------------------|----------------------------|
| https://support.atlassian.com/bitbucket-cloud/docs/manage-webhooks/ | Bitbucket Webhooks         |
| https://api.slack.com/messaging/webhooks     | Slack Incoming Webhooks    |
| https://docs.github.com/en/developers/webhooks-and-events/webhooks | GitHub Webhooks            |
| https://docs.gitlab.com/ee/user/project/integrations/webhooks.html | GitLab Webhooks            |
