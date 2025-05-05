---
title: Variables & Data Handling
description: Learn how to work with variables and data in your workflows
weight: 6
---

# Variables and Data Handling

Variables are essential for building dynamic and reusable workflows in AutoCRUD. They allow you to store, transform, and pass data between nodes in your flows, making your automations more powerful and flexible.

## Types of Variables

AutoCRUD supports several types of variables:

### Global Variables

Global variables are available across all flows in your workspace:

- Accessible from any flow
- Set through the Variables section
- Great for configuration values, API keys, etc.
- Centralized management for easier updates

<!-- GLOBAL VARIABLES SCREENSHOT -->
<!-- ![Global Variables](/images/global-variables.png) -->

### Flow Variables

Flow variables are specific to a single flow:

- Defined within a flow
- Used for flow-specific data
- Not accessible from other flows
- Reset with each flow execution

### Node Output Variables

Each node in your flow produces output that can be used as variables:

- Automatically available to downstream nodes
- Referenced using a special syntax
- Contains all data produced by the node
- Structured as objects with properties

## Working with Variables

### Accessing Variables

You can access variables in most node configuration fields using the following syntax:

- **Global Variables**: `{{ globals.variableName }}`
- **Flow Variables**: `{{ flow.variableName }}`
- **Node Outputs**: `{{ nodes.nodeName.output.propertyName }}`

<!-- VARIABLE SYNTAX SCREENSHOT -->
<!-- ![Variable Syntax](/images/variable-syntax.png) -->

### Setting Variables

There are multiple ways to set variable values:

1. **Global Variables Dashboard**:

   - Navigate to the Variables section
   - Click "Add Variable"
   - Enter name, description, and value
   - Save changes

2. **Set Variable Node**:

   - Add a "Set Variable" node to your flow
   - Configure variable name and value
   - Connect it in your flow

3. **Node Outputs**:
   - Output from each node is automatically available as variables
   - No explicit action needed to create these variables

### Variable Scope and Lifecycle

Understanding variable scope is important:

- **Global Variables**: Persist across all flows and executions
- **Flow Variables**: Exist only during a single flow execution
- **Node Output Variables**: Available only to downstream nodes in the same execution

## Data Transformation

AutoCRUD provides several ways to transform and manipulate data:

### Using Expressions

Use expressions to transform data:

```
{{ nodes.inputNode.output.value * 2 }}
```

```
{{ "Hello, " + nodes.nameInput.output.name }}
```

### JSON Transformation Node

For complex data transformations:

1. Add a "Transform" node to your flow
2. Define the transformation using a mapping interface
3. Connect it to input and output nodes

<!-- TRANSFORM NODE SCREENSHOT -->
<!-- ![Transform Node](/images/transform-node.png) -->

### Code Node

For advanced transformations:

1. Add a "Code" node to your flow
2. Write JavaScript/TypeScript code
3. Access input variables and produce output

```javascript
// Example code in a Code node
const input = $input;
const transformed = {
  fullName: `${input.firstName} ${input.lastName}`,
  age: input.age,
  isAdult: input.age >= 18,
};
return transformed;
```

## Data Types

AutoCRUD workflows support various data types:

- **Strings**: Text values
- **Numbers**: Numeric values
- **Booleans**: True/false values
- **Arrays**: Lists of values
- **Objects**: Key-value pairs
- **Dates**: Date and time values
- **Null**: Empty/no value

Each data type has specific operations and functionality available.

## Working with Arrays

Arrays (lists) are commonly used in workflows:

### Iterating Over Arrays

Process each item in an array:

1. Add a "Loop" node to your flow
2. Connect it to a node that outputs an array
3. Configure subsequent nodes to process each item

<!-- LOOP NODE SCREENSHOT -->
<!-- ![Loop Node](/images/loop-node.png) -->

### Array Operations

Perform common array operations:

- **Map**: Transform each item in an array
- **Filter**: Select items matching criteria
- **Reduce**: Combine array items into a single value
- **Find**: Locate specific items in an array

## Working with Objects

Objects (key-value pairs) help organize complex data:

### Accessing Object Properties

Access properties using dot notation:

```
{{ nodes.userData.output.user.address.city }}
```

### Creating and Modifying Objects

Create or modify objects using expressions:

```
{
  "name": {{ nodes.inputNode.output.name }},
  "email": {{ nodes.inputNode.output.email }},
  "createdAt": {{ "now" | date }}
}
```

## Best Practices

Follow these best practices for effective variable usage:

- **Descriptive Names**: Use clear, descriptive variable names
- **Documentation**: Add descriptions to global variables
- **Type Consistency**: Maintain consistent data types
- **Default Values**: Provide default values when possible
- **Validation**: Validate variable values before using them
- **Security**: Don't store sensitive data in plaintext variables
- **Organization**: Group related variables logically

## Common Variable Patterns

### Configuration Variables

Store configuration in global variables:

- API endpoints
- Default values
- Feature flags
- Environment-specific settings

### Data Passing

Pass data between different parts of your flow:

- Store intermediate results
- Pass user inputs through multiple steps
- Accumulate results across iterations

### Conditional Logic

Use variables for dynamic behavior:

- Change flow behavior based on variable values
- Implement different paths based on data
- Toggle features on/off

## Troubleshooting Variables

Common issues and solutions:

### Variable Not Found

If a variable isn't available:

1. Check the variable name and syntax
2. Verify the node producing the variable is upstream
3. Check for typos in the variable reference
4. Ensure the variable is within scope

### Incorrect Data Type

If a variable has the wrong data type:

1. Use transformation nodes to convert the type
2. Add explicit type conversion in expressions
3. Validate data earlier in the flow

### Variable Value Unexpected

If a variable doesn't contain expected data:

1. Add a "Debug" node to inspect the variable value
2. Check upstream nodes for correct output
3. Verify the data source is providing expected values
