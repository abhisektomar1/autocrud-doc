---
title: Triggers
description: Learn about different ways to start your workflows
weight: 2
---

# Flow Triggers

Triggers are the starting points of your workflows. They determine when and how your flow will be executed. AutoCRUD offers several trigger types to suit different automation needs.

## Available Trigger Types

### On Schedule Trigger

Schedule your workflows to run at specific times or intervals.

**Features:**

- Run on a cron schedule (e.g., every hour, daily, weekly)
- Set specific dates and times for execution
- Configure timezone settings

**Use Cases:**

- Daily data synchronization
- Weekly report generation
- Periodic cleanup tasks

<!-- SCHEDULE TRIGGER SCREENSHOT -->
<!-- ![Schedule Trigger](/images/schedule-trigger.png) -->

### HTTP Trigger

Trigger your workflows via webhooks when external events occur.

**Features:**

- Unique webhook URL for each flow
- Support for GET, POST, PUT, DELETE methods
- Access to request headers, body, and query parameters

**Use Cases:**

- Integrating with third-party services
- Responding to form submissions
- Processing webhook notifications

<!-- HTTP TRIGGER SCREENSHOT -->
<!-- ![HTTP Trigger](/images/http-trigger.png) -->

### On Demand Trigger

Manually trigger your workflows when needed.

**Features:**

- Simple button to execute the flow
- Optional input parameters
- Immediate execution

**Use Cases:**

- Testing workflows during development
- One-time data processing tasks
- Manual approval processes

<!-- ON DEMAND TRIGGER SCREENSHOT -->
<!-- ![On Demand Trigger](/images/on-demand-trigger.png) -->

## Configuring Triggers

### Basic Configuration

1. Click on the trigger node in your flow
2. Select the desired trigger type
3. Configure the specific settings for that trigger
4. Save your changes

### Advanced Options

Depending on the trigger type, you may have access to advanced options:

- **Retry Settings**: Configure automatic retries on failure
- **Timeout Settings**: Set maximum execution time
- **Input Parameters**: Define expected input data
- **Error Handling**: Configure actions on trigger failure

## Best Practices

- **Choose the Right Trigger**: Select the most appropriate trigger type for your automation needs
- **Document Webhook URLs**: Keep track of webhook URLs for HTTP triggers
- **Test Thoroughly**: Always test your triggers before deploying to production
- **Monitor Execution**: Regularly check trigger execution logs for issues
- **Set Reasonable Schedules**: Avoid scheduling too many flows at the same time

## Examples

### Daily Database Backup

```
Trigger Type: On Schedule
Schedule: Daily at 2:00 AM
```

### Customer Support Ticket Handler

```
Trigger Type: HTTP
Method: POST
Endpoint: /api/tickets
```

### Manual Data Import Process

```
Trigger Type: On Demand
Input Parameters: File Path
```

## Troubleshooting

If your trigger isn't working as expected:

1. Check the trigger configuration settings
2. Verify that any external systems are sending data correctly
3. Review execution logs for error messages
4. Test the trigger manually if possible
5. Ensure your workflow has the necessary permissions
