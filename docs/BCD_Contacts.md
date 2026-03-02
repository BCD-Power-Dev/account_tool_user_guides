# BCD Contacts Manager — User Guide

## Overview

The BCD Contacts Manager is a custom component for managing travel program contact records. It provides a central location to view, search, create, edit, and delete contact entries associated with your organization's GCN (Global Customer Number), SMID (Site/Market ID), and LCN (Local Customer Number) hierarchy.

Each contact record can store a title, contact details (name, email, phone, mobile, fax), rich-text notes, and organizational assignments across multiple GCN, SMID, and LCN values.

---

## Interface Layout

The component is split into two panels:

| Panel | Description |
|-------|-------------|
| **Left Sidebar** | Contact list with search, category filter, and the Add button |
| **Right Detail View** | Full detail for the selected contact, including notes, metadata, and edit/delete actions |

![Layout Overview](docs/layout-overview.png)

---

## Navigating Contacts

### Browsing the List

The left sidebar displays all contacts matching the current filter. Each list item shows:

- **Contact title** (bold when selected)
- **Contact type** badge (e.g. Contacts, Management, Operations)
- **SMID** and **LCN** indicator badges (when assigned)

Click any contact in the list to view its full details in the right panel.

### Searching

Use the **Search contacts…** field at the top of the sidebar to find contacts by title or name. The list filters in real time as you type.

### Filtering by Contact Type

Below the search field, a **dropdown filter** lets you narrow the list to a specific contact type. The component defaults to showing **Management** contacts on load.

Available filter options include:

- **All Types** — show every contact
- **Contacts** — general contact entries
- **Management** — management-level contacts *(default)*
- **Operations** — operations team contacts
- **Central Ticketing** — central ticketing contacts

The count next to each option shows how many contacts match that type.

---

## Viewing Contact Details

When you select a contact, the right panel displays:

### Header Section

- **Title** — the contact's display name
- **Contact Type** badge (blue)
- **GCN**, **SMID**, and **LCN** count badges showing how many of each are assigned
- **Last Updated** timestamp and the name of the user who last modified the record
- **Edit** (pencil icon) and **Delete** (trash icon) buttons in the top-right corner

### Contact Information Card

A summary card showing:

| Field | Description |
|-------|-------------|
| **Name** | The individual's name |
| **Email** | Email address |
| **Phone** | Primary phone number |
| **Mobile** | Mobile phone number |
| **Fax** | Fax number |

Fields that are empty will display a dash (—).

### Notes Card

The notes section renders rich-text content with support for:

- **Bold** and *italic* text
- Headings
- Bulleted and numbered lists
- Hyperlinks
- Blockquotes

> **Note:** Legacy HTML content from older records is automatically converted to readable markdown when displayed.

---

## Adding a New Contact

1. Click the **+ Add** button in the top-right corner of the sidebar.
2. The right panel switches to the **+ New Contact** form.
3. Fill in the required and optional fields:

| Field | Required | Description |
|-------|----------|-------------|
| **Title** | ✅ Yes | The contact's display title |
| **Contact Type** | No | Select from the dropdown (Contacts, Management, Operations, Central Ticketing) |
| **Name** | No | Individual's name |
| **Email** | No | Email address |
| **Phone** | No | Primary phone number |
| **Mobile** | No | Mobile number |
| **Fax** | No | Fax number |
| **Notes** | No | Rich-text notes with markdown toolbar |
| **GCN** | No | One or more Global Customer Numbers |
| **SMID** | No | One or more Site/Market IDs |
| **LCN** | No | One or more Local Customer Numbers |

4. Click **Add Contact** to save, or **Cancel** to discard.

### Using the Notes Editor

The notes field includes a **markdown toolbar** with the following buttons:

| Button | Action |
|--------|--------|
| **B** | Bold — wraps selected text in `**bold**` |
| *I* | Italic — wraps selected text in `*italic*` |
| **H** | Heading — prefixes the line with `### ` |
| • | Bullet List — prefixes lines with `- ` |
| 1. | Numbered List — prefixes lines with `1. `, `2. `, etc. |
| 🔗 | Link — inserts `[link text](url)` template |
| ❝ | Blockquote — prefixes the line with `> ` |

Select text first, then click a toolbar button to apply formatting. You can also type markdown syntax directly.

### Assigning GCN Values

The **GCN** field accepts comma-separated GCN codes. To add GCN values:

1. Type one or more GCN codes separated by commas (e.g. `4865, 486500`)
2. Press **Enter** or click outside the field
3. Each code appears as a removable tag
4. Click the **×** on any tag to remove it

### Assigning SMID Values

The **SMID selector** displays all available site/market options as a checkbox grid:

- Click any SMID tile to toggle selection (highlighted in blue when selected)
- Use **Select All** to check every SMID
- Use **Clear** to uncheck all
- The counter shows how many are selected (e.g. `SMID (3/150)`)
- Each tile shows the SMID name and country code

### Assigning LCN Values

The **LCN selector** works the same way as SMID:

- Click LCN tiles to toggle selection (highlighted in purple when selected)
- Use **Select All** or **Clear** for bulk actions
- The counter tracks your selections

---

## Editing a Contact

1. Select the contact you want to edit from the sidebar.
2. Click the **pencil icon** (✏️) in the detail header.
3. The right panel switches to the **Edit Contact** form, pre-filled with the current values.
4. Make your changes to any field.
5. Click **Save** to apply changes, or **Cancel** to discard.

> **Note:** When editing, the GCN, SMID, and LCN selectors will be pre-populated with the contact's current assignments. If none are set, they default to the currently selected account/site context.

---

## Deleting a Contact

1. Select the contact you want to delete from the sidebar.
2. Click the **trash icon** (🗑️) in the detail header.
3. A **red confirmation bar** appears at the bottom of the detail view:

   > Delete "Contact Title"? &nbsp; `[Cancel]` `[Delete]`

4. Click **Delete** to permanently remove the record, or **Cancel** to keep it.

> ⚠️ **Warning:** Deletion is permanent and cannot be undone.

---

## Understanding Badges and Indicators

Throughout the interface, colored badges provide quick context:

| Badge | Color | Meaning |
|-------|-------|---------|
| Contact type (e.g. "Management") | 🔵 Blue | The contact's category |
| GCN: *n* | 🟢 Teal | Number of GCN accounts assigned |
| SMID: *n* | 🟡 Amber | Number of SMID sites assigned |
| LCN: *n* | 🟢 Green | Number of LCN locations assigned |
| SMID (sidebar) | 🟡 Amber | Contact has SMID assignments |
| LCN (sidebar) | 🟢 Green | Contact has LCN assignments |

---

## Quick Reference

| Action | How |
|--------|-----|
| **Find a contact** | Type in the search box or use the type filter dropdown |
| **View details** | Click a contact in the sidebar |
| **Add a contact** | Click **+ Add** → fill form → click **Add Contact** |
| **Edit a contact** | Select contact → click ✏️ → update fields → click **Save** |
| **Delete a contact** | Select contact → click 🗑️ → confirm with **Delete** |
| **Change filter** | Use the dropdown below the search box |
| **Assign GCN** | Type codes separated by commas → press Enter |
| **Assign SMID/LCN** | Click tiles in the selector grid or use Select All / Clear |

---

## FAQ

**Q: Why do I only see Management contacts when I first open the component?**
The filter defaults to Management on load. Use the dropdown to switch to "All Types" or another category.

**Q: The notes look different from what I entered — why?**
Older records stored notes as HTML rich text. The component automatically converts this to readable markdown for display. When you edit and save, the cleaned markdown version is stored going forward.

**Q: Can a contact belong to multiple GCN accounts or SMID sites?**
Yes. A single contact record can be assigned to any number of GCN, SMID, and LCN values simultaneously. This is useful for contacts that serve multiple regions or accounts.

**Q: Who can edit or delete contacts?**
Edit and delete actions are only visible when your account has edit permissions enabled. If you don't see the pencil and trash icons, contact your administrator.

**Q: What does the count on the SMID badge mean?**
The number indicates how many SMID sites are assigned to that contact. For example, "SMID: 66" means the contact is associated with 66 different site/market IDs. Click into the edit form to see the full list.
