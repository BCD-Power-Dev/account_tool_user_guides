# Home
## Operational Knowledge Tool Overview
The new tool replaces the OKB account tool. Previous Account information that was stored in SharePoint has been migrated. There are several implementation phases that will be released based on the functions built into the new tool. 
## Access
### Agent/User
All standard users have read access only. Content edits or requests will be forwarded to supervisors/managers/ops teams for content update requests.
### Editors
The editor will have custom access to Add/Edit policy and related items similar to OKB. 
## Navigation
Overview of segments within the tool
### Account Selection
```

┌───────────────────────────────┐
│        Account Selection      │
└───────────────┬───────────────┘
                │
     ┌──────────┼───────────────────────────────────────────────────┐
     │              │               │               │               │
     ▼              ▼               ▼               ▼               ▼
┌───────────┐  ┌─────────────────────┐  ┌─────────────────────┐  ┌───────────┐
│ GCN Level │  │ Country (SMID) Level│  │ Entity (LCN/TSPM)   │  │ Favorites │
└───────────┘  └─────────────────────┘  │ Level               │  └───────────┘
                                        └─────────────────────┘         ▼
                                                         ┌──────────────┼─────────────┐
                                                ┌──────────────────────┐  ┌──────────────────┐  
                                                │ Country (SMID) Fav   │  │ Entity (LCN) Fav │ 
                                                └──────────────────────┘  └──────────────────┘
```
#### GCN Level
![Video Placeholder](https://raw.githubusercontent.com/BCD-Power-Dev/account_tool_user_guides/blob/main/docs/images/account_selection_land.gif)

- Search by GCN / Name
- Preview/Select Filtered Country (SMID) based on selected GCN
- Option to select Country(SMID) or View Entities (LCN/TSPM)
#### Country (SMID) Level
<img src="https://raw.githubusercontent.com/BCD-Power-Dev/account_tool_user_guides/blob/main/docs/images/select_smid.gif" width="100%" alt="Video Placeholder">

- SMID Selection only
#### Entity (LCN/TSPM) Level
<img src="https://raw.githubusercontent.com/BCD-Power-Dev/account_tool_user_guides/blob/main/docs/images/select_entity_2.gif" width="100%" alt="Video Placeholder">

- Entity Selection only
#### Favorites
<img src="https://raw.githubusercontent.com/BCD-Power-Dev/account_tool_user_guides/blob/main/docs/images/select_fav_2.gif" width="100%" alt="Video Placeholder">

- Country (SMID)
- Entity (LCN/TSPM)

### Summary
```
┌───────────────────────────────┐
│          Summary (Main)       │
└───────────────┬───────────────┘
                │
                ▼
┌────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                                    Account Summary                                                         │
└──────────────┬──────────────┬──────────────┬───────────────────────────┬─────────────────────┬──────────────┬─────────────┘
               │              │              │                           │                     │              │
               ▼              ▼              ▼                           ▼                     ▼              ▼
┌──────────────────────┐ ┌───────────────┐ ┌───────────────┐ ┌────────────────────────────┐ ┌───────────────────┐ ┌────────────┐
│    Account Detail    │ │    Status     │ │   PCC / OID   │ │ Standard Form of Payment   │ │ Deal/Disc Codes   │ │  Contacts  │
└───────────┬──────────┘ └───────────────┘ └───────────────┘ └────────────────────────────┘ └───────────────────┘ └────────────┘
            │                    │                     │                     │                      │
            ▼                    ▼                     ▼                     ▼                      ▼
┌───────────────────┐  ┌─────────────┐     ┌───────────────────┐    ┌────────────────────┐   ┌───────────────────────┐
│ TSPM Number       │  │   OBT       │     │ Region of Service │    │ Point of Sale Tool │   │ Daytime Ops Hours     │
├───────────────────┤  └─────────────┘     ├───────────────────┤    └────────────────────┘   └───────────────────────┘
│ GDS               │                      │ Ops Region        │
├───────────────────┤                      ├───────────────────┤
│ GDS Profile Name  │                      │ Country of Serv.  │
├───────────────────┤                      ├───────────────────┤
│ Traveler Profile  │                      │ BCD Team          │
├───────────────────┤                      ├───────────────────┤
│ GCN               │                      │ HPA               │
├───────────────────┤                      ├───────────────────┤
│ SMID              │                      │ APA               │
├───────────────────┤                      ├───────────────────┤
│ SQL ID            │                      │ Trip Authorizer   │
├───────────────────┤                      ├───────────────────┤
│ Back Office 1     │                      │ NDC               │
├───────────────────┤                      └───────────────────┘
│ Cust# / LCN 1     │
├───────────────────┤
│ DK 1              │
├───────────────────┤
│ Back Office 2     │
├───────────────────┤
│ Cust# / LCN 2     │
├───────────────────┤
│ DK 2              │
├───────────────────┤
│ Acct Type/Segment │
├───────────────────┤
│ L1 Profile        │
├───────────────────┤
│ L2 Profile        │
├───────────────────┤
│ HR Feed           │
├───────────────────┤
│ HR Feed Freq      │
├───────────────────┤
│ E-Invoice Portal  │
├───────────────────┤
│ E-Invoice Location│
└───────────────────┘
```
### Policy
#### General & Core
<img src="https://raw.githubusercontent.com/BCD-Power-Dev/account_tool_user_guides/blob/main/docs/images/policy_overview.gif" width="100%" alt="Video Placeholder">

##### General
The previous OKB section that housed technology has been replaced by a general one that AI has summarized into major categories. The General policy tab also includes:
- General
- Passport/Visa
- Country/Security Risks
- Travel Bookers
- OBT
- Reportable Fields
- Form of Payment (FOP)
##### Policy
<img src="https://raw.githubusercontent.com/BCD-Power-Dev/account_tool_user_guides/blob/main/docs/images/policy_detail.gif" width="100%" alt="Video Placeholder">

Policy is migrated to topics from OKB. The policy section now includes child topics so a parent topic can have nested topics. Air, Car, Hotel, Rail, Ground, Ferry, Taxi/Limo tabs include:
- Traveler Types
  - Fare Class Rules (by Traveler Type)
  - Policy (by Traveler Type)
  - Form of Payment (by Traveler Type)
  - Process (by Traveler Type)
  - Approval Process (by Traveler Type)
- Savings/Reason Codes
- Contract Detail
- Document (By category selected)
### Technology/Process
TBD
### Documents
<img src="https://raw.githubusercontent.com/BCD-Power-Dev/account_tool_user_guides/blob/main/docs/images/Document_Overview.gif" width="100%" alt="Video Placeholder">

General Document repository based on GCN level. The document will be opened in a new tab. Documents are stored in the SharePoint Document Library. 
### ESS
TBD

