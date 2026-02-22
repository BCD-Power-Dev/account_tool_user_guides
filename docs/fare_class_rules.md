# Fare Class Rules — User Guide

## Overview

Fare Class Rules define the conditions under which specific fare classes are applied for air travel bookings. Each rule is a structured set of up to **6 conditions** connected by **logic operators** and **criteria units** that together form a readable policy statement.

---

## How Rules Are Displayed

Each rule renders as a **narrative sentence** built from the conditions and logic you enter. For example:

> **US/CA Senior Management** is **less than or equal to** : **25** % : above the lowest fare **or** : Economy & Premium Economy **less than or equal to** : **10** % : in Business & First

This narrative is constructed from the fields you fill in, reading left to right.

---

## Rule Structure

### Boolean Flags

Every rule starts with three checkboxes that define where the rule applies:

| Flag | Description |
|------|-------------|
| **Domestic** | Rule applies to domestic travel (within country) |
| **International** | Rule applies to international travel (cross-border) |
| **Lowest Logical Fare** | Rule relates to lowest logical fare (LLF) policy |

You can check one or more. These appear as icons on the rule card:
- 🏠 House icon = Domestic
- 🌐 Globe icon = International
- 🎫 LLF icon = Lowest Logical Fare

---

### Conditions & Logic Fields

Rules use a **paired structure** where conditions describe "what" and logic/criteria describe "how":

```
┌─────────────────────────────────────────────────────────────┐
│  Condition 1          │  Fare Class Logic 1                 │
│  (what the rule is)   │  (comparison operator)              │
├───────────────────────┼─────────────────────────────────────┤
│  Condition 2          │  Condition 2 Criteria               │
│  (value/threshold)    │  (unit: %, €, $, etc.)              │
├───────────────────────┼─────────────────────────────────────┤
│  Condition 3          │  Fare Class Logic 2                 │
│  (additional context) │  (connector: and, or, etc.)         │
├───────────────────────┼─────────────────────────────────────┤
│  Condition 4          │  Fare Class Logic 3                 │
│  (second rule part)   │  (comparison operator)              │
├───────────────────────┼─────────────────────────────────────┤
│  Condition 5          │  Condition 5 Criteria               │
│  (value/threshold)    │  (unit: %, €, $, etc.)              │
├───────────────────────┴─────────────────────────────────────┤
│  Condition 6  (full width — final qualifying statement)     │
└─────────────────────────────────────────────────────────────┘
```

### Field Reference

| Field | Type | Purpose | Example Values |
|-------|------|---------|----------------|
| **Condition 1** | Text (free entry) | Primary rule description — what the rule applies to | `Europe`, `US/CA Senior Management`, `Domestic Travel Definition` |
| **Fare Class Logic 1** | Dropdown (logic) | Comparison operator for Condition 1 | `equal`, `less than or equal to`, `not equal` |
| **Condition 2** | Text (free entry) | Threshold value, region, or elaboration | `25`, `100`, `Within Europe` |
| **Condition 2 Criteria** | Dropdown (criteria) | Unit of measurement for Condition 2 | `%`, `€`, `$`, `£` |
| **Condition 3** | Text (free entry) | Additional qualifying text | `above the lowest fare` |
| **Fare Class Logic 2** | Dropdown (logic) | Connector between rule parts | `and`, `or` |
| **Condition 4** | Text (free entry) | Second rule part (fare class or category) | `Economy & Premium Economy` |
| **Fare Class Logic 3** | Dropdown (logic) | Comparison for the second part | `less than or equal to`, `equal` |
| **Condition 5** | Text (free entry) | Second threshold value | `10` |
| **Condition 5 Criteria** | Dropdown (criteria) | Unit for Condition 5 | `%`, `€`, `$` |
| **Condition 6** | Text (free entry) | Final qualifying statement (full width, no logic pair) | `in Business & First` |

---

## How the Narrative Is Built

The rule card displays a narrative sentence constructed from filled-in fields, joined by ` : ` separators. Logic operators appear in **bold**. Empty fields are skipped automatically.

### Formula

```
[Condition 1] is [Logic 1] : [Condition 2] [Criteria 2] : [Condition 3] [Logic 2] : [Condition 4] [Logic 3] : [Condition 5] [Criteria 5] : [Condition 6]
```

### Examples

#### Simple Rule (2 conditions)
| Field | Value |
|-------|-------|
| Condition 1 | `Europe` |
| Logic 1 | `less than or equal to` |
| Condition 2 | `100` |
| Criteria 2 | `€` |

**Displays as:** Europe is **less than or equal to** : **100** €

---

#### Complex Rule (6 conditions)
| Field | Value |
|-------|-------|
| Condition 1 | `US/CA Senior Management` |
| Logic 1 | `less than or equal to` |
| Condition 2 | `25` |
| Criteria 2 | `%` |
| Condition 3 | `above the lowest fare` |
| Logic 2 | `or` |
| Condition 4 | `Economy & Premium Economy` |
| Logic 3 | `less than or equal to` |
| Condition 5 | `10` |
| Criteria 5 | `%` |
| Condition 6 | `in Business & First` |

**Displays as:** US/CA Senior Management is **less than or equal to** : **25** % : above the lowest fare **or** : Economy & Premium Economy **less than or equal to** : **10** % : in Business & First

---

#### LLF Definition Rule
| Field | Value |
|-------|-------|
| Condition 1 | `Lowest Logical Airfare` |
| Logic 1 | `equal` |
| Condition 2 | `(lowest reasonable flight price) is the lowest available flight price within the search parameters` |

**Displays as:** Lowest Logical Airfare is **equal** : **(lowest reasonable flight price) is the lowest available flight price within the search parameters**

---

## Required Selections

### Traveler Type (Required)
Every rule must be associated with at least one **Traveler Type**. You can select multiple traveler types — they appear as green tags below the conditions.

Examples: `Standard Profiled Employee`, `HCP`, `VVIP`, `Delegation`, `Administration`

### SMID
The Service Management ID links the rule to a specific service profile. Pre-selected based on the current page context. Multiple SMIDs can be selected — they appear as blue tags.

### LCN
The Location/Cost Center Number links the rule to a specific business unit. Pre-selected based on the current page context.

---

## Adding a New Rule

1. Click the **+ Add Rule** button in the header
2. Check the applicable **boolean flags** (Domestic, International, Lowest Logical Fare)
3. Fill in **Condition 1** and select **Fare Class Logic 1** — this is the minimum required
4. Add additional conditions as needed (Conditions 2–6)
5. Select one or more **Traveler Types** (required)
6. Verify the **SMID** and **LCN** selections
7. Click **Add Rule**

**Tip:** You don't need to fill in all 6 conditions. Only fill in what's needed — empty fields are automatically skipped in the narrative.

---

## Editing a Rule

1. Click the **pencil icon** (✏️) on any rule card
2. The card expands into an edit form with all current values pre-filled
3. Modify any fields
4. Click **Save** to update, or **Cancel** to discard changes

---

## Deleting a Rule

1. Click the **trash icon** (🗑️) on any rule card
2. A confirmation prompt appears: "Delete this rule?"
3. Click **Yes, Delete** to permanently remove the rule, or **Cancel** to keep it

---

## Logic Operators Reference

These values are available in the **Fare Class Logic** dropdowns and are managed in the `fare_class_rules_logic` database table:

| Operator | Usage |
|----------|-------|
| `equal` | Exact match |
| `not equal` | Does not match |
| `less than or equal to` | At or below a threshold |
| `and` | Both conditions must apply |
| `or` | Either condition can apply |

---

## Criteria Units Reference

These values are available in the **Criteria** dropdowns and are managed in the `condition_criteria` database table:

| Unit | Usage |
|------|-------|
| `%` | Percentage |
| `€` | Euros |
| `$` | US Dollars |
| `£` | British Pounds |

---

## Auto-Populated Fields

The following fields are automatically managed by the system and do not need to be entered manually:

| Field | How It's Populated |
|-------|-------------------|
| `account_id` | Looked up from the GCN (Global Customer Number) |
| `smid_id` | Looked up from the SMID number(s) |
| `lcn_id` | Looked up from the LCN number(s) |
| `traveler_type_id` | Looked up from the Traveler Type name(s) |
| `updated_by` | Set to the current logged-in user |
| `last_updated` | Set to the current timestamp on save |

