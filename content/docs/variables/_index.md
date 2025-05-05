---
title: Variables
description: Learn how to create and manage global variables in your workspace
weight: 7
---

# Variables in AutoCRUD

Variables in AutoCRUD allow you to define and manage global values that can be used across your workspace. They provide a central place to store important values that may be used in multiple flows or settings.

## What You'll Learn

- How to create and manage global variables
- Ways to use variables in flows and automations
- Best practices for variable management
- Security considerations for sensitive variables

## Accessing Variables

To access the Variables section:

1. Navigate to your workspace
2. Click on the **Variables** item in the left sidebar

<!-- VARIABLES SECTION SCREENSHOT -->
<!-- ![Variables Section](/images/variables-section.png) -->

## Understanding Variables

Variables in AutoCRUD consist of two main components:

- **Key**: A unique identifier for the variable
- **Value**: The data stored in the variable

Variables are global to your workspace, meaning they can be accessed from any flow or automation within that workspace.

## Creating Variables

To create a new variable:

1. Navigate to the Variables section
2. Click the **Add Variable** button in the top-right corner
3. In the dialog that appears:
   - Enter a unique **Key** for your variable
   - Enter the **Value** for your variable
   - Optionally enable encryption for sensitive values
4. Click **Create Variable** to save

<!-- ADD VARIABLE SCREENSHOT -->
<!-- ![Add Variable Dialog](/images/add-variable-dialog.png) -->

### Variable Keys

When creating variable keys:

- Use descriptive names that clearly indicate the variable's purpose
- Avoid spaces and special characters
- Consider using a consistent naming convention
- Remember that keys are case-sensitive

**Examples of good variable keys:**

- `api_base_url`
- `defaultTaxRate`
- `companyName`
- `email_template_id`

### Variable Values

Variable values can be:

- Text strings
- Numbers
- JSON data (stored as a string)
- API keys or credentials (preferably encrypted)

### Encrypting Sensitive Variables

For sensitive information such as API keys or passwords:

1. When creating or editing a variable, check the **Encrypt this variable** option
2. The value will be stored securely and displayed as asterisks (**\*\*\***) in the interface
3. The variable can still be used in flows, but its actual value will not be visible in the UI

## Managing Variables

### Searching for Variables

If you have many variables, you can use the search function:

1. Enter your search term in the **Search variables...** box
2. The list will filter to show only variables that match your search

### Editing Variables

To modify an existing variable:

1. Find the variable in the list
2. Click the **Edit** button in the Actions column
3. Update the value as needed
4. Click **Save** to apply your changes

### Deleting Variables

To remove a variable you no longer need:

1. Find the variable in the list
2. Click the **Delete** button in the Actions column
3. Confirm the deletion when prompted

> **Warning**: Deleting a variable may break flows that use it. Be sure to update any references to the variable before deletion.

## Using Variables in Flows

Variables can be referenced in various parts of your flows:

### In Flow Steps

You can use variables in flow steps using the following syntax:

```
{{variables.YOUR_VARIABLE_KEY}}
```

For example, to use a variable named `api_key` in an HTTP request:

```
Authorization: Bearer {{variables.api_key}}
```

### In Conditions

Variables can be used in conditional logic:

```
{{variables.threshold}} > 100
```

### In Data Transformations

Variables can be part of data transformations:

```
{{data.price * variables.taxRate}}
```

## Best Practices

### Organization

- Use a consistent naming convention
- Group related variables with common prefixes
- Document the purpose of each variable
- Regularly review and clean up unused variables

### Security

- Always encrypt sensitive values like API keys and passwords
- Limit who can access and edit variables
- Rotate sensitive variables periodically
- Don't store extremely sensitive information like private keys

### Performance

- Keep the number of variables manageable
- Use meaningful names to make variables easy to find
- Consider using structured data (JSON) for related values

## Troubleshooting

**Issue**: Variable not appearing in flows
**Solution**: Verify the variable name and check for case sensitivity

**Issue**: Encrypted variable showing asterisks when you need to see the value
**Solution**: You cannot view the original value of encrypted variables; you'll need to reset it if you've lost the original value

**Issue**: Variable changes not affecting flows
**Solution**: Some flows may cache variable values; try restarting the flow

## Next Steps

Now that you understand variables, learn about:

- [Connecting External Resources]({{< ref "/docs/resources/_index.md" >}})
- [Building Automated Workflows]({{< ref "/docs/flows/creating-flows.md" >}})
