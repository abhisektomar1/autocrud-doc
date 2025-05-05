---
title: Resources
description: Learn how to configure external and internal connections in your workspace
weight: 8
---

# Resources in AutoCRUD

Resources in AutoCRUD allow you to configure and manage connections to external services and APIs. These connections can then be used in your flows to integrate with third-party systems and extend the functionality of your workspace.

## What You'll Learn

- How to add and configure different types of resources
- Ways to manage API keys and external connections
- Best practices for resource management
- Security considerations for external integrations

## Accessing Resources

To access the Resources section:

1. Navigate to your workspace
2. Click on the **Resources** item in the left sidebar

<!-- RESOURCES SECTION SCREENSHOT -->
<!-- ![Resources Section](/images/resources-section.png) -->

## Understanding Resources

Resources in AutoCRUD represent connections to external systems and services. They provide a centralized way to manage:

- API credentials
- External service connections
- Authentication tokens
- Integration points

## Resource Types

AutoCRUD supports various types of resources:

### API Keys

Credentials for authenticating with external APIs:

- REST API keys
- OAuth tokens
- Service account credentials
- Personal access tokens

### Database Connections

Connections to external databases:

- SQL databases
- NoSQL databases
- Data warehouses
- Cloud database services

### Integration Platforms

Connections to third-party integration services:

- Zapier
- IFTTT
- Microsoft Power Automate
- MuleSoft

### Storage Services

Connections to external storage:

- AWS S3
- Google Cloud Storage
- Azure Blob Storage
- Dropbox

## Adding a New Resource

To add a new resource:

1. Navigate to the Resources section
2. Click the **Add Resource** button (or similar option in your interface)
3. In the dialog that appears:
   - Select the resource type
   - Enter the required connection details
   - Configure any additional settings
4. Test the connection if available
5. Save the resource

<!-- ADD RESOURCE SCREENSHOT -->
<!-- ![Add Resource Dialog](/images/add-resource-dialog.png) -->

## Managing Resources

### Searching for Resources

If you have many resources, you can use the search function:

1. Enter your search term in the **Search resources...** box
2. Optionally, use the **Filter by Type** dropdown to narrow down results
3. The list will filter to show only resources that match your criteria

### Viewing Resource Details

To see details about a particular resource:

1. Find the resource in the list
2. Click on it to view its details
3. You'll see information such as:
   - Type of resource
   - Date added
   - Connection status
   - Usage statistics (if available)

### Editing Resources

To modify an existing resource:

1. Find the resource in the list
2. Click the menu (⋮) button for that resource
3. Select **Edit** from the menu
4. Update the settings as needed
5. Save your changes

### Deleting Resources

To remove a resource you no longer need:

1. Find the resource in the list
2. Click the menu (⋮) button for that resource
3. Select **Delete** from the menu
4. Confirm the deletion when prompted

> **Warning**: Deleting a resource may break flows that use it. Be sure to update any references to the resource before deletion.

## Using Resources in Flows

Resources can be used in various parts of your flows:

### In HTTP Requests

For API resources:

1. In a HTTP Request node, select the resource from the dropdown
2. The authentication headers will be automatically included
3. Configure the endpoint path and method as needed

### In Database Operations

For database connections:

1. In a Database Query node, select the database resource
2. Write your query or select operations
3. The connection details will be handled automatically

## Security Considerations

### Protecting Sensitive Resources

- All credentials are encrypted at rest
- API keys and tokens are never displayed in plain text after creation
- Access to resources is controlled by workspace permissions
- Consider using environment-specific resources for development vs. production

### Best Practices

- Regularly rotate API keys and credentials
- Use the principle of least privilege when creating service accounts
- Monitor usage of your resources to detect unusual activity
- Document the purpose and ownership of each resource

## Troubleshooting

**Issue**: Connection failed for a resource
**Solution**: Verify the credentials and ensure the external service is available

**Issue**: Resource not appearing in flows
**Solution**: Check resource permissions and ensure it's properly configured

**Issue**: Authentication errors when using a resource
**Solution**: The API key or token may have expired; try refreshing or regenerating it

## Next Steps

Now that you understand resources, learn about:

- [Managing Global Variables]({{< ref "/docs/variables/_index.md" >}})
- [Building Automated Workflows]({{< ref "/docs/flows/creating-flows.md" >}})
