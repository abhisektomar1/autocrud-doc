---
title: General Settings
description: Configure basic workspace information and settings
weight: 1
---

# General Settings

General settings allow you to manage the fundamental information about your workspace, including workspace name, description, and critical actions like deletion.

## Accessing General Settings

1. Navigate to your workspace
2. Click on the **Settings** icon in the left sidebar
3. Select the **General** tab

<!-- GENERAL SETTINGS SCREENSHOT -->
<!-- ![General Settings](/images/general-settings.png) -->

## Workspace Details

The Workspace Details section allows you to update basic information about your workspace:

### Workspace Name

Your workspace name identifies your workspace throughout the platform. A good name should:

- Clearly indicate the purpose of the workspace
- Be concise but descriptive
- Be easily recognizable by team members

To update your workspace name:

1. Enter the new name in the **Workspace Name** field
2. Click **Update Workspace** to save changes

### Description

The workspace description helps team members understand the purpose of the workspace. It should:

- Briefly explain what the workspace is used for
- Outline the main objectives or projects
- Provide context for new members

To update your description:

1. Enter the new description in the **Description** field
2. Click **Update Workspace** to save changes

## Danger Zone

The Danger Zone contains actions that can permanently affect your workspace. These actions require careful consideration before proceeding.

### Deleting a Workspace

Deleting a workspace is a permanent action that cannot be undone. When you delete a workspace:

- All tables, records, and views will be permanently removed
- All flows and automations will be deleted
- All workspace settings and configurations will be lost
- All members will lose access to the workspace

Before deleting a workspace, consider:

- Exporting important data for backup
- Informing all team members
- Verifying that you have the necessary permissions

To delete a workspace:

1. Navigate to the Danger Zone section at the bottom of General Settings
2. Review the warning message
3. Click the **Delete** button
4. Confirm the deletion in the prompt that appears

> **Warning**: Once deleted, all data will be permanently removed including all tables, views, and workflows. This action cannot be undone.

## Best Practices

- **Regular Updates**: Keep your workspace name and description up to date as projects evolve
- **Clear Communication**: Inform team members before making significant changes to workspace settings
- **Access Control**: Limit access to general settings to trusted administrators
- **Documentation**: Document important workspace settings for reference

## Troubleshooting

**Issue**: Changes not saving
**Solution**: Refresh the page and try again, ensure you have proper permissions

**Issue**: Cannot update workspace information
**Solution**: Verify you have admin privileges for the workspace

**Issue**: Error when trying to delete workspace
**Solution**: Ensure you're the workspace owner and all conditions for deletion are met

## Next Steps

After configuring general settings, you may want to explore:

- [Managing Access and Permissions]({{< ref "access.md" >}})
- [Customizing Workspace Appearance]({{< ref "appearance.md" >}})
