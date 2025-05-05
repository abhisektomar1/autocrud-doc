---
title: Table Views
description: Learn how to create and customize different views for your tables
weight: 2
---

# Table Views in AutoCRUD

Views provide different ways to visualize and interact with your table data. AutoCRUD offers multiple view types to help you organize, analyze, and work with your information effectively.

## Understanding Views

Views in AutoCRUD allow you to:

- Present the same data in different formats
- Create specialized interfaces for different purposes
- Save filters and sorting configurations
- Customize field visibility and arrangement
- Share specific perspectives with team members

<!-- VIEWS OVERVIEW SCREENSHOT -->
<!-- ![Views Overview](/images/views-overview.png) -->

## Available View Types

### Grid View

The most common view type, resembling a spreadsheet:

- Rows represent records
- Columns represent fields
- Inline editing capabilities
- Sorting and filtering options
- Resizable and reorderable columns

**Best for**: General data management, data entry, comprehensive overviews

<!-- GRID VIEW SCREENSHOT -->
<!-- ![Grid View](/images/grid-view.png) -->

### Kanban View

A board-style view that organizes records into columns based on a single select or status field:

- Visual organization of records
- Drag-and-drop functionality
- Customizable card appearance
- Color-coding by values
- Progress visualization

**Best for**: Project management, status tracking, workflow visualization

<!-- KANBAN VIEW SCREENSHOT -->
<!-- ![Kanban View](/images/kanban-view.png) -->

### Form View

A data entry-focused view that presents one record at a time in a form layout:

- Clean interface for data entry
- Field grouping and organization
- Required field validation
- Conditional field visibility
- Mobile-friendly design

**Best for**: Data collection, surveys, structured data entry

<!-- FORM VIEW SCREENSHOT -->
<!-- ![Form View](/images/form-view.png) -->

### Calendar View

Displays records with date fields in a calendar format:

- Day, week, month views
- Color-coding by field values
- Duration visualization
- Click-to-create functionality
- Event-style interactions

**Best for**: Scheduling, event planning, timeline visualization

### Gallery View

Presents records as cards in a grid layout with emphasis on visual elements:

- Image-focused presentation
- Customizable card layout
- Thumbnail previews
- Quick record browsing
- Visual filtering options

**Best for**: Media collections, product catalogs, visual data

## Creating and Managing Views

### Creating a New View

1. Open your table
2. Click the "+" icon next to the view tabs
3. Select the view type you want to create
4. Enter a name for the view
5. Configure view-specific settings
6. Click "Create View"

<!-- CREATE VIEW SCREENSHOT -->
<!-- ![Create View](/images/create-view.png) -->

### Customizing View Settings

Each view type has specific settings you can configure:

#### Grid View Settings

- Column width and order
- Frozen columns
- Row height
- Cell wrapping
- Conditional formatting

#### Kanban View Settings

- Grouping field selection
- Card content customization
- Column order and visibility
- Card size and layout
- Collapsed/expanded states

#### Form View Settings

- Field order and grouping
- Field size and layout
- Section headers
- Required fields
- Help text

### View-Specific Features

#### Grid View Features

**Column Configuration:**

1. Click on the column header
2. Use the dropdown menu to access options
3. Resize columns by dragging the column dividers
4. Reorder columns by dragging the column headers

**Row Actions:**

1. Hover over a row to see action buttons
2. Use context menu (right-click) for additional options
3. Select multiple rows for bulk actions

#### Kanban View Features

**Column Management:**

1. Add new columns through the "+" button
2. Reorder columns by dragging column headers
3. Collapse columns using the collapse icon
4. Configure column settings through the column menu

**Card Customization:**

1. Click "Customize cards" in the view menu
2. Select which fields to display on cards
3. Configure card size and layout
4. Set up custom card coloring rules

#### Form View Features

**Layout Customization:**

1. Enter design mode through the "Customize form" option
2. Drag fields to reposition them
3. Resize fields using handles
4. Add section headers and descriptions
5. Configure field properties

## Sharing and Collaborating with Views

### Sharing Specific Views

Share particular views with team members:

1. Open the view you want to share
2. Click the "Share" button
3. Choose sharing options:
   - Share with specific users
   - Share with entire workspace
   - Create a public link
4. Set permission levels (view only, edit, etc.)
5. Send the invitation or link

### View Permissions

Control what others can do with your views:

- **View Only**: Users can only see the data
- **Edit Data**: Users can edit records but not the view structure
- **Edit View**: Users can modify the view configuration
- **Manage**: Users have full control over the view

### Collaborative View Usage

Best practices for team collaboration:

- Create specialized views for different team roles
- Use consistent naming conventions for views
- Document the purpose of each view
- Regularly review and update view configurations
- Archive unused views to reduce clutter

## Advanced View Techniques

### Linked Record Views

When working with linked records:

1. Click on a linked record
2. Open the linked record in a new tab
3. Create specific views for linked record tables
4. Use lookups to display related data in the primary view

### Conditional Views

Create views with dynamic behavior:

1. Set up filters based on user or system values
2. Configure conditional formatting rules
3. Use formulas to drive view behavior
4. Set up conditional visibility for fields

### View Switching Automation

Automate view changes based on context:

1. Create links that open specific views
2. Set up default views for different user roles
3. Configure view redirects based on record state
4. Use URL parameters to control view selection

## View Templates and Examples

AutoCRUD offers several pre-built view templates:

- **Project Tracker**: Kanban view for task management
- **Customer Database**: Grid view with customer information
- **Event Calendar**: Calendar view for scheduling
- **Product Catalog**: Gallery view for products
- **Data Entry Form**: Form view for structured input

## Troubleshooting Views

### Common View Issues

**Issue**: View not displaying expected data
**Solution**: Check filters and sorting settings

**Issue**: View performance issues
**Solution**: Reduce the number of displayed fields or limit record count

**Issue**: Fields missing from view
**Solution**: Check field visibility settings in view configuration

**Issue**: Unable to modify view
**Solution**: Verify you have sufficient permissions for the view

## Next Steps

Now that you understand views, learn about:

- [Filtering and Sorting Data]({{< ref "filters-sorting.md" >}})
- [Working with Fields]({{< ref "fields.md" >}})
- [Table Relationships]({{< ref "relationships.md" >}})
- [Automating with Tables]({{< ref "/docs/flows/tables-integration.md" >}})
