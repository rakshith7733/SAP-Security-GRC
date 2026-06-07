# Creating and Maintaining User Master Data

## USERS
An SAP User is an account created in SAP that allows authentication and authorization.

```python
Note: 
    If there are many clients like 410,400,420 then we need to create user account in all necessary systems. If we create in one client that doesn't applicable in other client.
```

### TCODE: SU01
 PATH: SU01 > UserID >> ENTER.

Tabs
 Address    - Personal Data, Comunication, & Company address.
 Logon Data - User Type, Validity, Password, Usergroup.
 SNC        - Secure Communication on in the network.
 Default    - Start Menu, Logon Language, Date and time format, printer settings.
 Parameters - Default user parameters.
 Roles      - User roles and validity of roles assigned.
 Profiles   - User profiles, and roles wise pulled profiles.
 Personalization - User personalization data
 License Data - User License Agreement.

Example: PWIPRUK - Employee SAP User ID
         SAP_BATCH - Background Jobs
         RFC_PI - Interface User
         FIREFIGHTER - Emergency access.

#### SAP User Types:
1. Dialog User (A):
       Most common user type.
        Used by: Employees,
                 End Users,
                 Consultants,
                 Administrators.
        Characterstics:
                 Interactive logons
                 SAP GUI Access
                 Fiori Access
                 Password Required.

        Real world scenario: PWIPRUK

2. System User (B):
       System to System Communications.

       Characterstics:
                 No interactive logon
                 Password never expires
                 RFC Communications
                 Background processing
        Ex: SYNITI_READ
            BATCH_USER

    Real world scenario: ECC communicating with S/4 Hana.

3. Communication User (C):
       Used for: External applications
                 Interfaces
                 RFC Connections
        Characterstics:
                 RFC Login
                 Password required
                 No Dialog access
        Real world scenario: Salesforce sending data into SAP.

4. Service User (S):
        Shared account

        Characterstics:
                Anonymous access
                Shared among multiple users
                No individual assignments
        Real world Scenario: Training Environment

Note: 
    Auditors generally don't encourage service users as it would be difficult to track and No accountability.

5. Reference User (L):
       Special User Type. Cannot login directly, if additional authorization required.

       - Temporary reporting access.

#### User Group
- It defines the what a user ID belongs to. Administrative segregations.
- Restrict who can modify users

Ex: PL2329 - poland
    DE3300 - Germany
    AUDIT  - External / Internal Auditor
    FIREFIGHTER - Firefighter user
    TEST   - Test user
    LEAVERS - Terminated / Archieve Users
    BASIS  - Basis users
    APM_SEC - Application Security

UserGroup is created with Transaction: SUGR

-----------------------------------------------------------------------------------------------------
#### Step-by-Step to create user:
    Open the User Maintenance Transaction (SU01)
               |
        Choose "CREATE"
               |
    Fill the "Address" Tab => {Name, Email, Phone, Department, Communication}
               |
        Assign Roles(Single, Derived, & Composite)
               |
        Set an Initial Password, User Type, Validity & User Group
               |
            Save the User
-----------------------------------------------------------------------------------------------------






