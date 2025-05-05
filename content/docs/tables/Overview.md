---
title: Creating Tables
description: Learn how to create and set up tables in AutoCRUD
weight: 1
---

# Creating and Managing Tables

Tables are the fundamental building blocks for storing and organizing your data in AutoCRUD. This guide walks you through creating, configuring, and managing tables effectively.

## What is a Table?

In AutoCRUD, a table is a collection of data organized in rows (records) and columns (fields). Tables provide a familiar spreadsheet-like interface while offering the power and flexibility of a database.

<!-- TABLE INTERFACE SCREENSHOT -->
<!-- ![Table Interface](/images/table-interface.png) -->

## Creating Your First Table

### Step 1: Access the Tables Section

1. Navigate to your workspace
2. Click on the **Tables** icon in the left sidebar
3. Click the **+ New Table** button in the top-right corner

### Step 2: Define Basic Table Information

In the table creation dialog:

1. Enter a **Table Name** (use a clear, descriptive name)
2. Optionally add a **Description** to help others understand the table's purpose
3. Select a **Table Icon** (optional)
4. Click **Create Table**

<!-- CREATE TABLE SCREENSHOT -->
<!-- ![Create Table Dialog](/images/create-table-dialog.png) -->

### Step 3: Define Fields (Columns)

After creating your table, you'll be prompted to add fields:

1. Click **+ Add Field** to add your first field
2. Enter a **Field Name**
3. Select the appropriate **Field Type** (Text, Number, Date, etc.)
4. Configure field-specific options
5. Click **Save** to add the field
6. Repeat for additional fields

#### Available Field Types

AutoCRUD offers a wide range of field types to match your data needs:

| Field Type       | Description                          | Use Cases                                 |
| ---------------- | ------------------------------------ | ----------------------------------------- |
| Single Line Text | Short text content                   | Names, titles, short descriptions         |
| Long Text        | Extended text content                | Descriptions, notes, comments             |
| Number           | Numeric values                       | Quantities, measurements, scores          |
| Decimal          | Precise decimal values               | Prices, percentages, measurements         |
| Date             | Date values                          | Due dates, start dates, birthdays         |
| Date & Time      | Date and time values                 | Scheduled events, timestamps              |
| Checkbox         | Boolean (true/false) values          | Status flags, completion markers          |
| Single Select    | Choose one option from a list        | Categories, statuses, priorities          |
| Multiple Select  | Choose multiple options              | Tags, features, attributes                |
| User             | References to workspace users        | Assignments, responsibilities             |
| Attachment       | Files and media                      | Documents, images, files                  |
| Link             | References to other records          | Relationships between records             |
| Formula          | Calculated values                    | Totals, averages, conditional logic       |
| Lookup           | Display values from linked records   | Showing related information               |
| Rollup           | Aggregate values from linked records | Sums, counts, averages of related records |

<!-- FIELD TYPES SCREENSHOT -->
<!-- ![Field Types](/images/field-types.png) -->

### Step 4: Add Records (Rows)

Once your fields are set up, you can add data to your table:

1. Click the **+ Add Record** button at the bottom of the table
2. Enter values for each field
3. Press Enter or click outside the record to save
4. Continue adding records as needed

## Managing Existing Tables

### Renaming a Table

1. Open the table you want to rename
2. Click on the table name at the top of the page
3. Enter the new name
4. Press Enter to save

### Adding or Modifying Fields

To add new fields to an existing table:

1. Open the table
2. Click the **+** button in the column header area
3. Define the new field as described above

To modify an existing field:

1. Click on the field name in the column header
2. Select **Field Settings** or **Edit Field**
3. Make your changes
4. Click **Save**

### Deleting a Table

When you no longer need a table:

1. Go to the Tables list in your workspace
2. Find the table you want to delete
3. Click the "..." (more options) menu
4. Select **Delete Table**
5. Confirm the deletion

> **Warning**: Deleting a table permanently removes all its data. This action cannot be undone. Consider creating a backup before deletion.

## Table Templates

AutoCRUD offers templates for common use cases to help you get started quickly:

1. When creating a new table, click **Start from Template**
2. Browse available templates by category
3. Select a template that matches your needs
4. Customize the pre-built structure as needed

Popular templates include:

- Project Tracker
- Customer CRM
- Inventory Management
- Event Planning
- Bug Tracker
- HR Employee Directory

<!-- TABLE TEMPLATES SCREENSHOT -->
<!-- ![Table Templates](/images/table-templates.png) -->

## Importing Data

To import existing data into a new or existing table:

1. Open the table or create a new one
2. Click the **Import** button in the toolbar
3. Select your data source:
   - CSV file
   - Excel spreadsheet
   - JSON file
   - Other database
4. Upload your file or connect to the data source
5. Map imported columns to table fields
6. Review and confirm the import
7. Click **Import Data**

## Best Practices

### Naming Conventions

- Use clear, descriptive names for tables and fields
- Be consistent with naming patterns
- Consider including a prefix for related tables
- Avoid special characters in names

### Field Organization

- Group related fields together
- Order fields logically (e.g., basic info first, details later)
- Use field descriptions to provide context
- Consider what fields should be required vs. optional

### Data Integrity

- Use appropriate field types for your data
- Set up validations to ensure data quality
- Use select fields for consistent categorical data
- Consider relationships between tables

## Next Steps

Now that you've created your table, learn about:

- [Working with Fields]({{< ref "fields.md" >}})
- [Creating and Managing Views]({{< ref "views.md" >}})
- [Filtering and Sorting Data]({{< ref "filters-sorting.md" >}})
- [Setting Up Table Relationships]({{< ref "relationships.md" >}})
