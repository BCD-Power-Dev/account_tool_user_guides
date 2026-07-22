# Policy Manager - User Guide

> A guide for managing travel policy topics in the Policy Manager interface.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Interface](#understanding-the-interface)
3. [Working with Parent Topics](#working-with-parent-topics)
4. [Working with Subtopics](#working-with-subtopics)
5. [Editing Topics](#editing-topics)
6. [Using Markdown Formatting](#using-markdown-formatting)
7. [Assigning Traveler Types](#assigning-traveler-types)
8. [Assigning SMID and LCN](#assigning-smid-and-lcn)
9. [Searching Topics](#searching-topics)
10. [Tips & Best Practices](#tips--best-practices)

---

## Getting Started

The Policy Manager allows you to create, organize, and maintain policy documentation for different travel segments:

- **Air** - Flight booking policies
- **Rail** - Train travel policies
- **Car** - Car rental policies
- **Hotel** - Accommodation policies
- **Ground** - Ground transportation policies
- **Ferry** - Ferry travel policies
- **Limo** - Limousine service policies

Each segment has its own tab where you can manage policies specific to that travel type.

---

## Understanding the Interface

The Policy Manager is divided into two main areas:

```
┌─────────────────────────────────────────────────────────────┐
│                    Policy Manager                            │
├───────────────────────┬─────────────────────────────────────┤
│                       │                                     │
│   📁 Topic List       │         Topic Details               │
│                       │                                     │
│   ┌─────────────┐     │   Topic Name: [Title]               │
│   │ 📁 Parent 1 │     │                                     │
│   │   📄 Child  │     │   Detail:                           │
│   │   📄 Child  │     │   [Content with formatting]         │
│   │ 📁 Parent 2 │     │                                     │
│   │ 📁 Parent 3 │     │   Last Updated: [Date]              │
│   │   📄 Child  │     │   Updated By: [User]                │
│   └─────────────┘     │                                     │
│                       │   Traveler Types: [Tags]            │
│   [+ Add Topic]       │   SMID: [Tags]                      │
│   [🔍 Search...]      │   LCN: [Tags]                       │
│                       │                                     │
└───────────────────────┴─────────────────────────────────────┘
```

### Left Panel - Topic List
- Shows all policy topics in a tree structure
- **📁 Folders** = Parent topics (can contain subtopics)
- **📄 Files** = Subtopics (nested under parents)
- Click the **arrow** to expand/collapse parent topics
- Click any topic to view its details

### Right Panel - Topic Details
- Shows the full content of the selected topic
- Displays metadata (last updated, updated by)
- Shows assigned traveler types, SMID, and LCN
- Contains Edit and Delete buttons (if you have permission)

---

## Working with Parent Topics

Parent topics are the main categories that organize your policies. They appear as folders in the topic list.

### Adding a New Parent Topic

1. Click the **[+]** button in the top-right of the topic list
2. Fill in the **Add New Topic** form:
   - **Topic Name** - Enter a clear, descriptive title (required)
   - **Detail** - Add the policy content (supports Markdown formatting)
   - **Traveler Types** - Select which traveler types this applies to
   - **SMID** - Select applicable SMIDs
   - **LCN** - Select applicable LCNs
3. Click **Save Topic**

### Example Parent Topics

Good parent topic names are clear and categorical:
- ✅ "Booking Policies"
- ✅ "Cancellation Rules"
- ✅ "Fare Class Guidelines"
- ✅ "Price Assurance"

---

## Working with Subtopics

Subtopics provide detailed information under a parent topic. They appear as document icons nested under their parent.

### Adding a New Subtopic

1. **Hover** over a parent topic in the list
2. Click the **[📄+]** icon that appears
3. Fill in the **Add Subtopic** form:
   - The parent topic is shown at the top for reference
   - **Subtopic Name** - Enter a descriptive title
   - **Detail** - Add the detailed policy content
   - Assign traveler types, SMID, and LCN as needed
4. Click **Save Subtopic**

### Example Subtopic Structure

```
📁 Price Assurance (Parent)
   📄 APA - Overview
   📄 APA - Fare Search Rules
   📄 APA - Eligible Bookings
   📄 APA - Exceptions
```

---

## Editing Topics

### To Edit a Topic

1. **Select** the topic by clicking on it in the list
2. Click the **Edit** button in the details panel
3. The form switches to edit mode:
   - Modify the topic name
   - Update the detail content
   - Change traveler type assignments
   - Update SMID/LCN selections
4. Click **Save** to apply changes
5. Click **Cancel** to discard changes

### What Gets Tracked

Every edit automatically records:
- **Timestamp** - When the change was made
- **User** - Who made the change
- **Version** - Edit history is preserved

---

## Using Markdown Formatting

The detail field supports Markdown formatting for rich text content.

### Formatting Toolbar

The toolbar above the detail field provides quick formatting buttons:

| Button | Format | Example |
|--------|--------|---------|
| **B** | Bold | `**text**` → **text** |
| *I* | Italic | `*text*` → *text* |
| 🖍️ | Highlight | `==text==` → ==highlighted== |
| H1 | Heading 1 | `# Title` |
| H2 | Heading 2 | `## Section` |
| H3 | Heading 3 | `### Subsection` |
| 📊 | Table | Insert table template |
| 🔗 | Link | `[text](url)` |
| • | List | `- item` |
| `</>` | Code | `` `code` `` |

### Common Formatting Examples

#### Bold and Italic
```markdown
**This is bold text**
*This is italic text*
***This is bold and italic***
```

#### Headings
```markdown
# Main Title
## Section Header
### Subsection
#### Minor Header
```

#### Lists
```markdown
- First item
- Second item
- Third item
```

#### Links
```markdown
[Click here for more info](https://example.com)
```

#### Tables
```markdown
| Column 1 | Column 2 | Column 3 |
| --- | --- | --- |
| Data | Data | Data |
```

#### Highlighted Text
```markdown
This is ==important highlighted== information.
```

### Preview

While editing, a **Preview** section below the editor shows how your formatting will appear.

---

## Assigning Traveler Types

Traveler types determine which travelers a policy applies to.

### Selecting Traveler Types

1. In the edit form, find the **Traveler Types** section
2. Click on traveler types to select/deselect them:
   - ☑️ Checked = Policy applies to this type
   - ☐ Unchecked = Policy does not apply
3. Use **Select All** to check all types
4. Use **Clear** to uncheck all types

### Common Traveler Types

- Standard Profiled Employee
- VIP/Executive
- Contractor
- Supplier
- Training Travel
- Recruit/Candidate

---

## Assigning SMID and LCN

SMID and LCN control which markets and locations see specific policies.

### SMID (Market ID)

1. Find the **SMID** section in the edit form
2. Select applicable markets by clicking on them
3. Selected markets appear with a blue highlight
4. Use **Select All** / **Clear** for bulk selection

### LCN (Location Number)

1. Find the **LCN** section in the edit form
2. Select applicable locations
3. Selected locations appear with a purple highlight

### Tips

- If no SMID/LCN is selected, the policy may apply globally (check with your admin)
- You can select multiple SMIDs and LCNs per topic
- Filtered views show only policies matching the current SMID/LCN context

---

## Searching Topics

Use the search bar to quickly find topics.

### How to Search

1. Click in the **Search topics...** field
2. Type your search term
3. Results filter in real-time as you type

### What Gets Searched

- Topic names
- Topic content/details

### Search Tips

- Search is case-insensitive
- Partial matches work ("cancel" finds "Cancellation")
- Matching terms are highlighted in results
- Clear the search box to show all topics again

---

## Tips & Best Practices

### Organizing Topics

1. **Use clear, descriptive names** - Make it easy to find topics later
2. **Group related policies** - Use parent topics as categories
3. **Keep subtopics focused** - One specific policy per subtopic
4. **Use consistent naming** - Establish naming conventions with your team

### Writing Good Policy Content

1. **Start with the key information** - Put the most important points first
2. **Use headings to organize** - Break up long policies into sections
3. **Include examples** - Help users understand with concrete examples
4. **Keep it current** - Update policies when rules change
5. **Use formatting sparingly** - Don't over-highlight; it reduces impact

### Before You Delete

⚠️ **Deleting is permanent!** Before deleting a topic:
- Make sure no one needs the information
- Consider archiving or updating instead
- Note that deleting a parent topic may affect reporting

### Getting Help

If you encounter issues:
1. Check that you have edit permissions (admin, builder, or Content_Editor role)
2. Refresh the page if changes aren't appearing
3. Contact your system administrator for access issues

---

## Quick Reference

| Action | How To |
|--------|--------|
| Add parent topic | Click [+] button → Fill form → Save |
| Add subtopic | Hover parent → Click [📄+] → Fill form → Save |
| Edit topic | Select topic → Click Edit → Make changes → Save |
| Delete topic | Select topic → Click Delete → Confirm |
| Search | Type in search box |
| Expand/collapse | Click arrow next to parent topic |

---

## Keyboard Shortcuts

Currently, all actions are performed via mouse/touch. Future versions may include keyboard shortcuts.

---

*For technical documentation or troubleshooting, contact your system administrator.*
