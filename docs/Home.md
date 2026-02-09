# Home
## Operational Knowledge Tool Overview
The new tool replaces the OKB account tool. Previous Account information that was stored in sharepoint has been migrated. There are several implementation phases that will be released based on the function builds in the new tool. 
## Access
### Agent/User
All standard users have read access only. Content edits or request will be forwarded to supervisors/managers/ops teams for content update request.
### Editors
### Content Support Teams
## Support
Overview of the support conditions
## Navigation
Overview of segments within the tool
### Account Selection
```text
┌───────────────────────────────┐
│        Account Selection      │
└───────────────┬───────────────┘
                │
 ┌──────────────┼───────────────┬───────────────┬───────────────┐
 │              │               │               │               │
▼              ▼               ▼               ▼
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
- Search by GCN / Name
- Preview/Select Filtered Country (SMID) based on selected GCN
- Option to select Country(SMID) or View Entities (LCN/TSPM)
#### Country (SMID) Level
- SMID Selection only
#### Entity (LCN/TSPM) Level
- Entity Selection only
#### Favorites
- Country (SMID)
- Entity (LCN/TSPM)

### Summary
```text
┌───────────────────────────────┐
│          Summary (Main)       │
└───────────────┬───────────────┘
                │
                ▼
                ┌─────────────────────┼───────────────┼──────────────────────┼──────────────────────────────┼──────────────────┼───────────┼────────────────┼──────────────────────────┐
                │                     │               │                      │                              │                  │           │                │                          │
                ▼                     ▼               ▼                      ▼                              ▼                  ▼           ▼                ▼                          ▼
┌──────────────────────────┐  ┌──────────────┐  ┌─────────────┐  ┌──────────────────────────────┐┌─────────────────────┐  ┌──────────┐  ┌─────┐  ┌──────────────────────┐ ┌───────────────────────────┐
│       Account Detail     │  │    Status    │  │  PCC / OID  │  │   Standard Form of Payment   ││ Deal/Discount Codes │  │ Contacts │  │ OBT │  │ Point of Sale Tool   │ │ Daytime Operational Hours │
└──────────────┬───────────┘  └──────────────┘  └─────────────┘  └──────────────────────────────┘└─────────────────────┘  └──────────┘  └─────┘  └──────────────────────┘ └───────────────────────────┘
               │                     
     ┌─────────┼──────────────────────────────────────────────────┐      
     │                           │                                │
     ▼                           ▼                      ▼     
 ┌───────────────────┐  ┌───────────────────┐  ┌───────────────────┐ 
 │ TSPM Number       │  │ Region of Service │  │ HPA               │  
 └───────────────────┘  └───────────────────┘  └───────────────────┘
 ┌───────────────────┐  ┌───────────────────┐  ┌───────────────────┐
 │ GDS               │  │ Ops Region        │  │ APA               │
 └───────────────────┘  └───────────────────┘  └───────────────────┘
 ┌───────────────────┐  ┌───────────────────┐  ┌───────────────────┐
 │ GDS Profile Name  │  │ Country of Service│  │ Trip Authorizer   │
 └───────────────────┘  └───────────────────┘  └───────────────────┘ 
 ┌───────────────────┐  ┌───────────────────┐  ┌───────────────────┐
 │ Traveler Profile  │  │ BCD Team          │  │ NDC               │
 └───────────────────┘  └───────────────────┘  └───────────────────┘                   
 ┌───────────────────┐    
 │ GCN               │   
 └───────────────────┘                      
 ┌───────────────────┐  
 │ SMID              │   
 └───────────────────┘                       
 ┌───────────────────┐  
 │ SQL ID            │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ Back Office 1     │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ Cust# / LCN 1     │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ DK  1             │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ Back Office 2     │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ Cust# / LCN 2     │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ DK 2              │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ Acct Type/Segment │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ L1 Profile        │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ L2 Profile        │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ HR Feed           │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ HR Feed Freq      │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ E-Invoice Portal  │   
 └───────────────────┘ 
 ┌───────────────────┐  
 │ E-Invoice Location│   
 └───────────────────┘ 

```
### Policy
### Technology/Process
### Documents
### ESS

