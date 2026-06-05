## SAP SECURITY and GRC {ECC /S4 HANA}

*Systems, Applications, and products in Data Processing(SAP):*
--> It is an enterprise Resource planning (ERP) software that helps organizations manage and integrate their business processes into a single system.

*What is SAP Security?*
--> It is the process of managing and controlling user access to SAP   systems and what actions they can perform. They ensure to perform business functions while maintaining compliance, security, & SODs.

*Objective:*
1. SAP Authorizations
2. Fundamentals of SAP Authorizations
3. SAP User Master
4. Role Maintenance
5. Authorization Development
6. Administrative settings
7. Transport Authorizations
8. Interface and Special Authorization
9. Central user Administration.
10. SAO Audit Information system.
11. Security Audit Tools
12. SAP Security Optimization.
13. Secure Network Communications.
--------------------------------------------------------------------
*SAP Architecture*
Three Tier Architecture
|
|---Presentation Layer (Interface)
|        |--- SAP GUI, Fiori Launchpad
|
|---Application Layer(SAP Business Logic)
|        |--- Authorization Checks, Business Rules, Workflows
|
|---Database Layer(Data Storage)
         |--- User Data, Material Data, Customer Data.

*SAP Landscape*

SAP System
│
├── SAP Basis
├── SAP ABAP
├── Functional Modules
│      ├── FI
│      ├── MM
│      ├── SD
│      └── HCM
│
└── SAP Security
        ├── Users
        ├── Roles
        ├── Authorizations
        ├── GRC
        └── Compliance
--------------------------------------------------------------------
SAP ECC
- Older ERP platform
- GUI Based environment.

SAP S/4 HANA
- SAP HANA Database
- Faster processing
- Fiori Applications
- Simplified Data Model
- Embeded Analytics

SAP Fiori:
- Modern SAP user Interface
- Uses SAP Fiori, Apps, Tiles, Launchpad

Ex: Purchase Order App
    Display Financial Report App

*Security in Day-to-Day life*

Assets
- Hardware
- Software
- Data


Threats
- Persons(Hackers)
- Environment(Floods)
- Technology(Data crash)

Measures
- Organizations(Procedures, trainings)
- Environment(Fire alarms)
- Technology(Hardware router, Data backup, password rules, Authorizations)
--------------------------------------------------------------------

*SAP Access Controls*

#### System Access Control:
- User must identify themselves in the system.
- Configuration of system access control(Ex. Password Rules).

#### Access Control:
- Access rights for functions and data must be granted explicitly using authorizations
- Authorization checks for
    - Transaction / Report calls.
    - Program Execution.

--------------------------------------------------------------------
*Technical Implementation of Roles*
"Business Purchase" Role

Role Menu:
- Accessible transactions, reports, web links and so on.
- Structure of the Menus / Access Paths

Authorizations:
- Selective access to business functions and data using profiles.



