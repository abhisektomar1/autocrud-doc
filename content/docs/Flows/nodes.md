---
title: Node Types
description: Explore all available nodes for building your workflows
weight: 3
---

# Flow Nodes

Nodes are the building blocks of your workflows in AutoCRUD. Each node performs a specific action, from sending emails to making HTTP requests to processing data. This guide covers all available node types and how to use them.

## Basic Nodes

### Send Email

Send emails through various providers like SMTP, AWS SES, and more.

**Key Features:**

- Configure sender and recipient information
- Support for HTML content
- Attachment capabilities
- Template variables support

**Configuration Options:**

- **To**: Recipient email address
- **Subject**: Email subject line
- **Body**: Email content
- **From**: Sender email address (optional)
- **CC/BCC**: Additional recipients (optional)

<!-- SEND EMAIL NODE SCREENSHOT -->
<!-- ![Send Email Node](/images/send-email-node.png) -->

### HTTP Request

Make API calls to external services or fetch data from the web.

**Key Features:**

- Support for all HTTP methods (GET, POST, PUT, DELETE, etc.)
- Custom headers and query parameters
- Authentication options
- JSON, XML, and form data handling

**Configuration Options:**

- **URL**: The endpoint to request
- **Method**: HTTP method to use
- **Headers**: Request headers
- **Body**: Request body content
- **Query Parameters**: URL parameters

<!-- HTTP REQUEST NODE SCREENSHOT -->
<!-- ![HTTP Request Node](/images/http-request-node.png) -->

### Ask Question

Leverage AI to generate responses to questions.

**Key Features:**

- Natural language processing
- Contextual understanding
- Customizable responses
- Integration with workflow variables

**Configuration Options:**

- **Question**: The prompt or query
- **Context**: Additional context information
- **Response Format**: How the answer should be structured

<!-- ASK QUESTION NODE SCREENSHOT -->
<!-- ![Ask Question Node](/images/ask-question-node.png) -->

## Advanced Nodes

### If Condition

Add branching logic to your workflows based on conditions.

**Key Features:**

- Multiple condition types
- Comparison operators
- Complex logical expressions
- Variable reference support

**Configuration Options:**

- **Condition Type**: Equal, Not Equal, Greater Than, etc.
- **Value A**: First value to compare
- **Value B**: Second value to compare
- **Operator**: AND, OR, NOT

### Generate Image

Create images using AI-powered image generation.

**Key Features:**

- Text-to-image conversion
- Style customization
- Size and format options
- Integration with other nodes

**Configuration Options:**

- **Prompt**: Description of the image to generate
- **Style**: Visual style preference
- **Size**: Dimensions of the output image
- **Format**: Output file format

### Embeddings

Generate vector embeddings for text and data.

**Key Features:**

- Convert text to vector representations
- Similarity search capabilities
- Integration with databases
- Support for various embedding models

**Configuration Options:**

- **Text**: Input text to convert
- **Model**: Embedding model to use
- **Dimensions**: Vector dimension size
- **Output Format**: How to structure the result

### Information Extractor Schema

Extract structured data from unstructured content.

**Key Features:**

- Intelligent field extraction
- Schema-based parsing
- Support for multiple input formats
- Customizable output structure

**Configuration Options:**

- **Input**: Text or data to process
- **Schema**: Definition of what to extract
- **Format**: Input format type
- **Output**: How to structure the result

### Content Moderation

Filter and analyze content for inappropriate material.

**Key Features:**

- Text and image moderation
- Customizable sensitivity levels
- Detailed analysis reports
- Automated actions based on results

**Configuration Options:**

- **Content**: Material to moderate
- **Categories**: Types of content to flag
- **Threshold**: Sensitivity level
- **Action**: What to do when content is flagged

## Working with Nodes

### Adding Nodes to a Flow

1. Click the "+" button in the flow builder
2. Select the desired node type from the menu
3. Position the node on the canvas
4. Connect it to other nodes in your flow

### Configuring Nodes

1. Click on a node to select it
2. Use the configuration panel on the right to set options
3. Required fields are marked with an asterisk (\*)
4. Click "Apply" or "Save" to confirm changes

### Connecting Nodes

1. Click and drag from the output handle of one node
2. Release on the input handle of another node
3. A connection line will appear between the nodes
4. Data will flow through this connection during execution

### Testing Node Output

Most nodes have a "Test" button that allows you to:

- Execute just that node
- View the output data
- Troubleshoot configuration issues
- Verify correct functionality

## Best Practices

- **Name Your Nodes**: Give descriptive names to make your flow easier to understand
- **Organize Your Layout**: Arrange nodes logically from left to right
- **Use Comments**: Add notes to explain complex parts of your workflow
- **Test Incrementally**: Verify each node works before connecting the next one
- **Handle Errors**: Include error handling for critical nodes

## Next Steps

Now that you understand the available nodes, learn how to implement [Error Handling]({{< ref "error-handling.md" >}}) in your flows.
