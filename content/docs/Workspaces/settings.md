---
title: Workspace Settings
description: Learn how to configure and manage workspace settings
weight: 2
---

# Managing Workspace Settings

Workspace settings allow you to customize your AutoCRUD environment to fit your team's needs. This guide covers all the configuration options available for your workspaces.

## Accessing Workspace Settings

1. Navigate to your workspace
2. Click on the **Settings** icon in the left sidebar
3. Select the appropriate settings category

<!-- SETTINGS MENU SCREENSHOT -->
<!-- ![Settings Menu](/images/workspace-settings-menu.png) -->

## General Settings

The General settings tab allows you to configure basic workspace information:

### Workspace Name and Description

- **Name**: Change your workspace name
- **Description**: Update the description to help team members understand the workspace purpose
- **Timezone**: Set the default timezone for the workspace

### Appearance

- **Theme**: Choose between light, dark, or system theme
- **Accent Color**: Select a primary color for your workspace interface
- **Logo**: Upload a custom logo for your workspace (Pro and Enterprise plans)

### Notifications

- **Email Notifications**: Configure email alerts for various workspace events
- **In-app Notifications**: Set preferences for notifications within the application
- **Digests**: Enable daily or weekly summary emails

## Members & Permissions

The Members section allows you to manage who has access to your workspace and what they can do:

### Inviting Members

1. Navigate to Settings > Members
2. Click **Invite Members**
3. Enter email addresses
4. Select role/permission level
5. Add optional message
6. Click **Send Invitations**

<!-- INVITE MEMBERS SCREENSHOT -->
<!-- ![Invite Members Interface](/images/invite-members-interface.png) -->

### User Roles

AutoCRUD offers several predefined roles:

| Role   | Description                   | Capabilities                                    |
| ------ | ----------------------------- | ----------------------------------------------- |
| Owner  | Full control of workspace     | Can do everything, including deleting workspace |
| Admin  | Administrative control        | Can manage settings, members, and content       |
| Editor | Can create and modify content | Can create and edit tables and flows            |
| Viewer | Read-only access              | Can only view tables and flows, cannot edit     |

### Custom Permissions

For more granular control (available on Pro and Enterprise plans):

1. Navigate to Settings > Members
2. Click **Custom Roles**
3. Create a new role or modify existing ones
4. Set specific permissions for tables, flows, variables, etc.
5. Assign custom roles to members

## Integrations

Manage third-party service connections:

### Available Integrations

- **Authentication Providers**: Google, GitHub, Microsoft, etc.
- **Communication Tools**: Slack, Discord, Microsoft Teams
- **Storage Services**: AWS S3, Google Cloud Storage, Dropbox
- **Email Providers**: SMTP, SendGrid, Mailgun
- **Analytics Tools**: Google Analytics, Mixpanel

### Setting Up Integrations

1. Navigate to Settings > Integrations
2. Select the service you want to connect
3. Follow the authentication process
4. Configure service-specific settings
5. Test the connection

<!-- INTEGRATIONS SCREENSHOT -->
<!-- ![Integrations Panel](/images/integrations-panel.png) -->

## Billing & Subscription

Manage your plan and payment details:

### Subscription Information

- View current plan details
- Check usage limits and current usage
- See billing cycle and next payment date

### Changing Plans

1. Navigate to Settings > Billing
2. Click **Change Plan**
3. Select the new plan
4. Confirm the change
5. Review prorated charges or credits

### Payment Methods

- Add, remove, or update payment methods
- View payment history
- Download invoices

## Security

Configure security settings for your workspace:

### Authentication Settings

- **Password Requirements**: Set minimum complexity requirements
- **Two-Factor Authentication**: Require 2FA for all workspace members
- **Session Management**: Configure timeout settings
- **Login Restrictions**: Limit login attempts, IP restrictions

### Data Protection

- **Encryption**: Configure data encryption settings
- **Backup Settings**: Set up regular backups
- **Data Retention**: Configure how long data is kept
- **Export Controls**: Manage who can export data

## Advanced Settings

Additional configuration options for advanced users:

### API Access

- Generate and manage API keys
- Configure API rate limits
- Set CORS settings for API access

### Custom Domain (Enterprise)

- Connect a custom domain to your workspace
- Configure SSL certificates
- Set up domain redirects

### Audit Logs

- View all actions performed in the workspace
- Filter logs by user, action type, date range
- Export logs for compliance purposes

<!-- AUDIT LOGS SCREENSHOT -->
<!-- ![Audit Logs](/images/audit-logs.png) -->

## Troubleshooting Settings Issues

### Common Issues

**Issue**: Changes not saving
**Solution**: Refresh the page and try again, ensure you have proper permissions

**Issue**: Integration connection failing
**Solution**: Verify credentials, check service status, review network settings

**Issue**: Cannot update billing information
**Solution**: Ensure you're an Owner or have billing admin privileges

## Best Practices

- **Regular Reviews**: Periodically review workspace settings, especially security settings
- **Documentation**: Document any custom configurations for team reference
- **Testing**: Test integrations after setting them up
- **Permissions Audit**: Regularly review member permissions
- **Backup Configuration**: Ensure proper backup settings are configured

## Next Steps

Now that you've configured your workspace settings, learn about:

- [Collaborating with Team Members]({{< ref "collaboration.md" >}})
- [Creating Tables and Views]({{< ref "/docs/tables/overview.md" >}})
- [Building Automated Workflows]({{< ref "/docs/flows/creating-flows.md" >}})
