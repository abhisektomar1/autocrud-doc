---
title: Creating Flows
description: Learn how to create and configure workflows
weight: 1
---

# Creating Your First Flow

AutoCRUD's visual flow builder makes it easy to create powerful automated workflows without writing code. This guide will walk you through creating your first flow.

## Prerequisites

- An AutoCRUD account with access to a workspace
- Basic understanding of the workflow concept

## Step 1: Access the Flows Section

1. Navigate to your workspace dashboard
2. Click on the **Flows** icon in the left sidebar
3. Click the **Create Flow** button in the top-right corner

<!-- CREATING FLOW SCREENSHOT -->
<!-- ![Create Flow Button](/images/flows-create-button.png) -->

## Step 2: Design Your Workflow

Once in the flow builder, you'll see a canvas where you can design your workflow:

1. Start with a **Trigger Node** (automatically added)
2. Use the **+** button or drag nodes from the node library to add actions
3. Connect nodes by dragging from the output of one node to the input of another

<!-- FLOW DESIGN SCREENSHOT -->
<!-- ![Flow Design Interface](/images/flow-design-interface.png) -->

## Step 3: Configure Your Trigger

Every flow starts with a trigger that determines when your workflow will run:

1. Click on the trigger node to open its configuration panel
2. Select a trigger type:
   - **On Schedule**: Run at specified intervals
   - **HTTP**: Triggered by a webhook
   - **On Demand**: Manually triggered
3. Configure the trigger settings as needed

<!-- TRIGGER CONFIGURATION SCREENSHOT -->
<!-- ![Trigger Configuration](/images/trigger-configuration.png) -->

## Step 4: Add and Configure Action Nodes

Add actions to your workflow to perform specific tasks:

1. Click on the + button to add a node
2. Select from available node types:
   - **Send Email**: Send email notifications
   - **HTTP Request**: Make API calls to external services
   - **Ask Question**: Leverage AI for question answering
   - And many more...
3. Configure each node's parameters as required

<!-- NODE CONFIGURATION SCREENSHOT -->
<!-- ![Node Configuration Panel](/images/node-config-panel.png) -->

## Step 5: Test Your Flow

Before deploying your flow, you should test it to ensure it works as expected:

1. Click the **Play** button in the toolbar to run your flow
2. Monitor the execution in real-time
3. Check node outputs to verify the results
4. Make adjustments as needed

## Step 6: Save and Activate Your Flow

Once you're satisfied with your flow:

1. Give your flow a descriptive name
2. Click the **Save** button
3. Activate your flow to make it live

## Example: Simple Email Notification Flow

Let's create a simple flow that sends an email when triggered:

1. Start with a trigger node (e.g., HTTP trigger)
2. Add a **Send Email** node
3. Connect the trigger to the email node
4. Configure the email node with recipient, subject, and content
5. Save and test your flow

<!-- EXAMPLE FLOW SCREENSHOT -->
<!-- ![Example Email Flow](/images/example-email-flow.png) -->

## Next Steps

Now that you've created your first flow, you can:

- Explore more complex workflows with multiple nodes
- Learn about [Advanced Triggers]({{< ref "triggers.md" >}})
- Discover all available [Node Types]({{< ref "nodes.md" >}})
- Implement [Error Handling]({{< ref "error-handling.md" >}}) in your flows
