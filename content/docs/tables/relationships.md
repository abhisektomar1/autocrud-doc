---
title: Table Relationships
description: Learn how to connect tables and work with relational data
weight: 5
---

# Table Relationships

One of the most powerful features of AutoCRUD is the ability to create relationships between tables. This allows you to connect related data and build complex data models similar to relational databases.

## Understanding Table Relationships

Table relationships in AutoCRUD allow you to:

- Connect records between different tables
- View related data in context
- Maintain data integrity
- Build sophisticated data models
- Reduce data duplication

<!-- RELATIONSHIPS DIAGRAM -->
<!-- ![Relationships Diagram](/images/relationships-diagram.png) -->

## Types of Relationships

AutoCRUD supports several relationship types:

### One-to-Many Relationship

The most common relationship type, where one record in Table A can be linked to multiple records in Table B.

**Example**: A Customer (Table A) can have multiple Orders (Table B).

### Many-to-Many Relationship

A relationship where records in both tables can link to multiple records in the other table.

**Example**: Students (Table A) can enroll in multiple Courses (Table B), and each Course can have multiple Students.

### One-to-One Relationship

A relationship where one record in Table A corresponds to exactly one record in Table B.

**Example**: An Employee (Table A) has one detailed Profile (Table B).

## Creating Table Relationships

### Step 1: Add a Link Field

1. Open the table where you want to create the link
2. Click **+ Add Field**
3. Select **Link to Another Record** as the field type
4. Choose the table you want to link to
5. Configure the relationship settings:
   - Relationship name
   - Field names in both tables
   - Reciprocal field settings
6. Click **Save** to create the relationship

<!-- LINK FIELD CREATION SCREENSHOT -->
<!-- ![Creating Link Field](/images/creating-link-field.png) -->

### Step 2: Configure Reciprocal Field (Automatic)

When you create a link field, AutoCRUD automatically creates a reciprocal field in the linked table:

- For One-to-Many: Creates a "Many" field in the linked table
- For Many-to-Many: Creates another "Many" field in the linked table
- For One-to-One: Creates a "One" field in the linked table

You can rename these reciprocal fields to better describe the relationship.

## Working with Linked Records

### Adding Links Between Records

To link records together:

1. Open the record you want to link from
2. Click in the link field cell
3. Search for or select the record(s) you want to link to
4. Click outside the cell to save

### Viewing Linked Records

When viewing a record with links:

1. The link field shows the linked records
2. Click on a linked record to expand details
3. Use the "+" icon to add more links
4. Use the "x" icon to remove links

### Expanding Linked Records

To see more details about linked records:

1. Click on the linked record
2. Select **Expand Record** to see full details
3. Navigate between linked records using the arrows

## Advanced Relationship Features

### Lookup Fields

Lookup fields display information from linked records directly in your table:

1. Add a new field to your table
2. Select **Lookup** as the field type
3. Choose the link field to use for the lookup
4. Select which field from the linked table to display
5. Configure display options

**Example**: In an Orders table with a link to Customers, add a lookup field to display the Customer's email or phone number directly in the Orders table.

<!-- LOOKUP FIELD SCREENSHOT -->
<!-- ![Lookup Field](/images/lookup-field.png) -->

### Rollup Fields

Rollup fields perform calculations on linked records:

1. Add a new field to your table
2. Select **Rollup** as the field type
3. Choose the link field to use for the rollup
4. Select which field from the linked table to aggregate
5. Choose the aggregation function (Sum, Average, Count, etc.)

**Example**: In a Projects table with links to Tasks, add a rollup field to count the total number of tasks or sum their estimated hours.

### Filtering Linked Records

When adding links, you can filter which records are available to link:

1. Click in a link field
2. Use the filter option in the record selector
3. Set conditions to narrow down the available records
4. Select from the filtered list

## Best Practices for Table Relationships

### Data Model Planning

- Plan your data model before creating complex relationships
- Diagram your tables and their connections
- Consider what types of queries you'll need to perform
- Think about data integrity and maintenance

### Naming Conventions

- Use clear, descriptive names for link fields
- Name link fields based on the relationship they represent
- Be consistent with naming patterns across your workspace
- Consider using prefixes for related fields

### Performance Considerations

- Avoid creating unnecessary relationships
- Be cautious with deeply nested lookups and rollups
- Consider breaking very complex relationships into simpler ones
- Use filters to limit the number of linked records when possible

## Common Use Cases

### Customer Relationship Management (CRM)

- Customers linked to Orders
- Contacts linked to Companies
- Activities linked to Customers
- Products linked to Orders

### Project Management

- Projects linked to Tasks
- Tasks linked to Team Members
- Projects linked to Clients
- Resources linked to Tasks

### Inventory Management

- Products linked to Categories
- Products linked to Suppliers
- Orders linked to Products
- Warehouses linked to Inventory Items

## Troubleshooting Relationships

### Common Issues

**Issue**: Cannot see reciprocal field
**Solution**: Check if the field was renamed or hidden; unhide the field in the field settings

**Issue**: Lookup or rollup field not updating
**Solution**: Refresh the view or check if the relationship is set up correctly

**Issue**: Difficulty selecting the right records to link
**Solution**: Use filters or improve naming conventions for clearer identification

## Next Steps

Now that you understand table relationships, learn about:

- [Building Automated Workflows with Tables]({{< ref "/docs/flows/tables-integration.md" >}})
