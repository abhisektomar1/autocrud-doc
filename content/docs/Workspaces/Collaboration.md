---
title: Collaboration
description: Learn how to collaborate effectively with your team in AutoCRUD
weight: 3
---

# Team Collaboration in Workspaces

AutoCRUD provides powerful collaboration features that allow teams to work together seamlessly on tables, flows, and other workspace components. This guide shows you how to collaborate effectively with your team.

## Collaboration Overview

With AutoCRUD's collaboration features, you can:

- Invite team members to workspaces
- Assign different permission levels
- Work simultaneously on the same tables and flows
- Track changes and activities
- Communicate within the platform
- Share and control access to resources

<!-- COLLABORATION FEATURES SCREENSHOT -->
<!-- ![Collaboration Features](/images/collaboration-features.png) -->

## Managing Team Members

### Inviting Team Members

1. Navigate to **Settings** > **Members** in your workspace
2. Click **Invite Members**
3. Enter email addresses (separate multiple addresses with commas)
4. Select the appropriate role for each member
5. Add an optional personal message
6. Click **Send Invitations**

New members will receive an email invitation with instructions to join your workspace.

### Member Roles and Permissions

AutoCRUD offers several predefined roles with different permission levels:

| Role   | Tables        | Flows         | Settings       | Members                | Billing     |
| ------ | ------------- | ------------- | -------------- | ---------------------- | ----------- |
| Owner  | Full access   | Full access   | Full access    | Can manage all members | Full access |
| Admin  | Full access   | Full access   | Limited access | Can manage non-owners  | View only   |
| Editor | Create & edit | Create & edit | No access      | No access              | No access   |
| Viewer | View only     | View only     | No access      | No access              | No access   |

### Creating Custom Roles

For more granular control (available on Pro and Enterprise plans):

1. Go to **Settings** > **Members** > **Roles**
2. Click **Create Custom Role**
3. Name your role
4. Configure specific permissions for each component
5. Save the new role
6. Assign it to existing or new members

<!-- CUSTOM ROLE SCREENSHOT -->
<!-- ![Custom Role Creation](/images/custom-role-creation.png) -->

## Real-time Collaboration

### Simultaneous Editing

Multiple team members can work on the same workspace simultaneously:

- **Tables**: Multiple users can edit different records at the same time
- **Flows**: Members can collaborate on workflow design
- **Comments**: Discuss changes directly within the interface

### Change Tracking

Keep track of who made which changes:

- View edit history for each record
- See who created or modified flows
- Track configuration changes
- Filter activity by user, date, or action type

<!-- ACTIVITY TRACKING SCREENSHOT -->
<!-- ![Activity Tracking](/images/activity-tracking.png) -->

## Communication Tools

### Comments

Leave comments directly in your workspace:

1. Select a record in a table
2. Click on the comments icon
3. Type your comment
4. @mention team members to notify them
5. Reply to existing comments

### Notifications

Stay informed about important changes:

- **In-app notifications**: Receive alerts within AutoCRUD
- **Email notifications**: Get updates via email
- **@mentions**: Get notified when someone mentions you
- **Custom alerts**: Set up notifications for specific events

## Sharing and Access Control

### Sharing Individual Resources

Share specific tables or flows with team members:

1. Open the table or flow you want to share
2. Click the **Share** button
3. Set access level (view, edit, manage)
4. Add users or teams
5. Enable/disable specific permissions
6. Save your sharing settings

### Public Sharing

Share resources with people outside your organization:

1. Open the resource you want to share
2. Click **Share** > **Get Link**
3. Configure link permissions:
   - Anyone with the link
   - Password-protected
   - Specific email domains
4. Set expiration date (optional)
5. Copy and share the link

<!-- PUBLIC SHARING SCREENSHOT -->
<!-- ![Public Sharing Options](/images/public-sharing-options.png) -->

## Best Practices for Team Collaboration

### Organization Structure

- **Clear Hierarchy**: Define a clear permission structure
- **Documentation**: Create documentation for team processes
- **Naming Conventions**: Use consistent naming for resources
- **Folder Structure**: Organize resources in logical folders

### Communication Guidelines

- **Regular Updates**: Keep team members informed about changes
- **Descriptive Comments**: Write clear comments that provide context
- **Status Indicators**: Use status fields to show progress
- **Change Logs**: Maintain logs of significant changes

### Security Considerations

- **Principle of Least Privilege**: Grant only necessary permissions
- **Regular Audits**: Review member access periodically
- **Offboarding Process**: Remove access when team members leave
- **Sensitive Data**: Mark and restrict access to sensitive information

## Troubleshooting Collaboration Issues

### Common Issues and Solutions

**Issue**: Member can't access shared resources
**Solution**: Verify their permission level and ensure the resource is shared correctly

**Issue**: Conflicting changes to the same record
**Solution**: Use the change history to review and resolve conflicts

**Issue**: Too many notifications
**Solution**: Adjust notification settings in your user preferences

**Issue**: Accidental deletion or changes
**Solution**: Use the version history to restore previous versions

## Next Steps

Now that you understand how to collaborate with your team, learn about:

- [Creating and Managing Tables]({{< ref "/docs/tables/overview.md" >}})
- [Building Automated Workflows]({{< ref "/docs/flows/creating-flows.md" >}})
