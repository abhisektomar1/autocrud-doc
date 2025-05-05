---
title: Tables & Flows Integration
description: Learn how to automate table operations with flows
weight: 7
---

# Integrating Tables with Flows

One of the most powerful features of AutoCRUD is the ability to connect your tables with automated workflows. This guide shows you how to use flows to automate operations on your tables, creating powerful data-driven applications.

## Understanding Table Automation

By connecting tables with flows, you can:

- Trigger workflows when table data changes
- Automatically update records based on conditions
- Process data and perform calculations
- Connect your table data with external services
- Build complete business processes around your data

<!-- TABLE AUTOMATION OVERVIEW -->
<!-- ![Table Automation Overview](/images/table-automation-overview.png) -->

## Table-Related Flow Triggers

### Record Created Trigger

Start a flow when a new record is created in a table:

1. Create a new flow
2. Select "Record Created" as the trigger type
3. Choose the table to monitor
4. Configure any additional options (filters, etc.)
5. The flow will run each time a new record is created

**Use cases**: Send welcome emails, create related records, initiate approval processes

### Record Updated Trigger

Trigger a flow when a record in a table is modified:

1. Create a new flow
2. Select "Record Updated" as the trigger type
3. Choose the table to monitor
4. Optionally specify which fields to watch for changes
5. Configure any additional filters

**Use cases**: Notification systems, status updates, audit logging, data synchronization

### Record Deleted Trigger

Run a flow when a record is deleted from a table:

1. Create a new flow
2. Select "Record Deleted" as the trigger type
3. Choose the table to monitor
4. Configure any additional options

**Use cases**: Cleanup related records, archive data, send notifications

### View Button Trigger

Add a custom button to a table view that triggers a flow:

1. Create a new flow
2. Select "View Button" as the trigger type
3. Choose the table and view
4. Configure the button appearance and behavior
5. The flow will run when users click the button

**Use cases**: Bulk operations, custom actions, process initiation

<!-- VIEW BUTTON TRIGGER SCREENSHOT -->
<!-- ![View Button Trigger](/images/view-button-trigger.png) -->

## Table Operation Nodes

AutoCRUD provides several nodes for interacting with tables in your flows:

### Create Record Node

Add new records to a table:

1. Add a "Create Record" node to your flow
2. Select the target table
3. Map data to the fields you want to populate
4. Configure additional options (error handling, etc.)

**Example**: Creating a customer record after a form submission

```
{
  "name": "{{trigger.data.name}}",
  "email": "{{trigger.data.email}}",
  "createdAt": "{{now()}}"
}
```

### Find Records Node

Query tables to find specific records:

1. Add a "Find Records" node to your flow
2. Select the table to query
3. Configure filter conditions
4. Specify sorting and limits if needed

**Example**: Finding all overdue tasks

```
{
  "where": {
    "dueDate": { "lt": "{{now()}}" },
    "status": { "ne": "Completed" }
  },
  "limit": 100,
  "sort": [{ "field": "dueDate", "direction": "asc" }]
}
```

### Update Record Node

Modify existing records in a table:

1. Add an "Update Record" node to your flow
2. Select the target table
3. Specify how to identify the record(s) to update
4. Define the fields and values to update

**Example**: Marking a task as completed

```
{
  "where": { "id": "{{trigger.data.recordId}}" },
  "update": {
    "status": "Completed",
    "completedAt": "{{now()}}"
  }
}
```

### Delete Record Node

Remove records from a table:

1. Add a "Delete Record" node to your flow
2. Select the target table
3. Specify how to identify the record(s) to delete
4. Configure confirmation and safety options

**Example**: Deleting old archive records

```
{
  "where": {
    "createdAt": { "lt": "{{addDays(now(), -365)}}" },
    "status": "Archived"
  }
}
```

## Common Automation Scenarios

### Data Enrichment

Automatically enhance records with additional data:

1. Trigger on record creation/update
2. Use HTTP Request nodes to fetch external data
3. Update the record with the enriched information

**Example**: Adding company information to a contact record by looking up their email domain

### Approval Workflows

Create multi-step approval processes:

1. Trigger when a record status changes to "Pending Approval"
2. Send notification to approvers
3. Create approval tasks or records
4. Update the original record based on approval decisions

### Data Synchronization

Keep multiple tables or systems in sync:

1. Trigger when records change
2. Transform data as needed
3. Update corresponding records in other tables or external systems
4. Log synchronization activities

### Notifications and Alerts

Send alerts based on table conditions:

1. Trigger on record updates
2. Check if conditions meet alert criteria
3. Send notifications via email, Slack, or other channels
4. Update record to acknowledge the alert

<!-- NOTIFICATION WORKFLOW SCREENSHOT -->
<!-- ![Notification Workflow](/images/notification-workflow.png) -->

## Advanced Table Automation Techniques

### Batch Processing

Process multiple records in a single flow run:

1. Use a scheduled trigger or manual button
2. Find records matching your criteria
3. Loop through the records
4. Process each record with your business logic
5. Update processing status

### Conditional Record Creation

Create records based on complex conditions:

1. Trigger on an event
2. Evaluate conditions using If nodes
3. Create different record types based on conditions
4. Link the new records appropriately

### Cascading Updates

Update related records automatically:

1. Trigger when a parent record changes
2. Find all related child records
3. Update the child records based on parent changes
4. Optionally trigger further workflows

### Form to Table Automation

Create complete data collection workflows:

1. Design a form view for data entry
2. Trigger a flow when the form is submitted
3. Validate and process the submitted data
4. Create records in multiple related tables
5. Send confirmation notifications

## Best Practices

### Performance Considerations

- Limit the frequency of triggers for high-volume tables
- Use indexing for fields used in filtering
- Batch operations when possible
- Implement error handling and retry logic
- Monitor flow execution times

### Data Integrity

- Validate data before creating or updating records
- Implement transaction-like patterns for multi-table updates
- Create audit trails for important changes
- Use rollback mechanisms for failed operations

### Maintenance and Monitoring

- Document your automations
- Set up monitoring for failed flows
- Review flow execution logs regularly
- Test flows thoroughly before deployment
- Use descriptive naming for flows and nodes

## Troubleshooting

### Common Issues

**Issue**: Flow not triggering on record changes
**Solution**: Check trigger configuration and ensure it matches the expected changes

**Issue**: Record updates not working
**Solution**: Verify record identification conditions and field mappings

**Issue**: Flow running too slowly
**Solution**: Optimize database queries, reduce complexity, batch operations

**Issue**: Circular update issues
**Solution**: Implement guards against recursive triggering

## Next Steps

Now that you know how to integrate tables with flows, explore:
