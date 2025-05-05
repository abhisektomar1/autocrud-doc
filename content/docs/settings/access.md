---
title: Access Management
description: Control who can access your workspace and set permissions
weight: 2
---

# Access Management

The Access Management section allows you to control who has access to your workspace and what level of permissions they have. This is essential for team collaboration while maintaining appropriate security controls.

## Accessing Access Management Settings

1. Navigate to your workspace
2. Click on the **Settings** icon in the left sidebar
3. Select the **Access** tab

<!-- ACCESS MANAGEMENT SCREENSHOT -->
<!-- ![Access Management](/images/access-management.png) -->

## Understanding User Roles

AutoCRUD offers different role types to control what users can do within your workspace:

| Role   | Description                   | Capabilities                                  |
| ------ | ----------------------------- | --------------------------------------------- |
| Admin  | Full administrative control   | Can manage settings, members, and all content |
| Editor | Can create and modify content | Can create and edit tables and flows          |
| Viewer | Read-only access              | Can only view tables and flows, cannot edit   |

## Inviting Collaborators

To invite new members to your workspace:

1. Click the **Invite Collaborator** button in the top-right corner
2. In the dialog that appears, enter the new member's email address
3. Select the appropriate role (Admin, Editor, or Viewer)
4. Click **Invite** to send the invitation

<!-- INVITE COLLABORATOR SCREENSHOT -->
<!-- ![Invite Collaborator](/images/invite-collaborator.png) -->

The invited collaborator will receive an email with instructions to join your workspace. Their status will show as "PENDING" until they accept the invitation.

## Managing Existing Collaborators

The Access Management page displays a list of all current collaborators with the following information:

- **Collaborator**: Email address and profile initial
- **Permission**: Current role assignment
- **Invited by**: Who sent the invitation
- **Status**: Whether the invitation is ACTIVE or PENDING
- **Invited On**: Date and time when the invitation was sent

### Changing Permissions

To change a collaborator's role:

1. Find the collaborator in the list
2. Click on their current role in the **Permission** column
3. Select the new role from the dropdown menu
4. The change takes effect immediately

### Removing Collaborators

To remove someone's access to your workspace:

1. Find the collaborator in the list
2. Click the three-dot menu (⋮) at the end of their row
3. Select **Delete** from the menu
4. Confirm the removal when prompted

## Finding Collaborators

If you have many collaborators, you can use the search function to find specific people:

1. Click the search field at the top of the collaborator list
2. Enter the name or email address you're looking for
3. The list will filter to show matching results

## Best Practices for Access Management

- **Principle of Least Privilege**: Grant only the permissions necessary for each user's role
- **Regular Audits**: Periodically review who has access to your workspace
- **Offboarding Process**: Immediately remove access when someone leaves your team
- **Role Documentation**: Document which roles are assigned to different team members
- **Clear Ownership**: Ensure there's always at least one Admin for each workspace

## Troubleshooting

**Issue**: Invitation email not received
**Solution**: Check spam folders, verify the email address, or resend the invitation

**Issue**: Cannot change a user's role
**Solution**: Ensure you have Admin permissions yourself

**Issue**: Too many collaborators
**Solution**: Check your subscription limits, you may need to upgrade your plan

**Issue**: Collaborator shows as PENDING for too long
**Solution**: Ask the collaborator to check their email or resend the invitation

## Next Steps

After setting up access management, you may want to explore:

- [Configuring General Settings]({{< ref "general.md" >}})
- [Customizing Workspace Appearance]({{< ref "appearance.md" >}})
- [Collaboration Features]({{< ref "/docs/Workspaces/Collaboration.md" >}})
