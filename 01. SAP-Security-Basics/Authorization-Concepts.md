### Authorization Concepts

Why do we require Authorizations?
- Security Expectations
- Protection of sensitive business data on basis of
    - Laws
    - Agreements
    - Regulations
- Advantageous cost benifit relation.
- No obstruction of business processes.

*Implementation methods and Authorizations*

##### Project Preparation >>> Business Blueprint >>> Realization >> Final Preparation >>> GO Live & Support |Live| >> Continuous Improvement.

Step1:
Get information from clients what are the requuirements

Step2:
Validate what are the effective roles to be performed, new to be created, what are the fields to be maintained. we need to have a full blueprint.

Step3:
Create roles:
           Single Role
           Imparting Role (Reference Role)
           Derived Role
           Composite Role
           Customizing role
Additionally need to check with Functional team for role contents.

Step4:
- Test user roles and authorizations with Positive and Negative checks.
- Train end users with new roles.
- Internal tests

Step5:
- Setup for production environment.
- Implement, test, and release new requirements in accordance with implementation requests.


#### Fundamentals of SAP Authorizations

What is Authorization? 
- It is a permission that allows a user to perform a specific activity within SAP
- Without authorization, SAP denies access.

Why?
- Security
- Data Confidentially
- Regulatory Compliance
- Segregation of Duties(SODs)

*Authorization Profile:*
- When a role is generated, SAP creates an authorization profile.
- The profile contains authorization data that assigned to users.

*Authorization Object:*
- They defines what SAP checks during execution.

Ex: ACTVT: Activity(01,02,03)
    WERKS: Plant(NL51,2000-2329)

*Most Common Authorization Objects*

    S_TCODE	    Transaction Access
    S_USER_GRP	User Groups
    S_USER_AGR	Role Administration
    S_USER_PRO	Profile Administration
    M_BEST_EKO	Purchasing Organization
    F_BKPF_BUK	Company Code Authorization

Field, Object, & Object Classes

    Authorization_Fields  Authorization_Objects  Authorization_Object_classes
        BUKRS                 M_RECH_BUK                  MM_R
        ACTVT                 F_KNA1_BUK                  FI
        WERKS                 M_MSEG_WWA                  MM_S
        BEGRU                 V_KNA1_BRG                  SD
      
   --> The above data is associate with each other to authorization object and respective object class based on the activity the user will able to access what was assigned in authorization objects in a transaction.


#### Elements of the SAP Authorization Concept
    Object Class         | Authorization Object | Authorization   | Profile     | Role  | User
    Financial Accounting | F_KNA1_BUK           | Fields & Values | T_58000097  | Z_ROLE | User master: PWIPRUK

1. Object Class: A logical group of authorization objects

       Ex: Material Management: Purchasing.


2. Authorization object: Defines what needs to be checked during authorization.
   - contains one or more authorization fields.

            Ex: Auth object: M_BEST_BSA
                Activity (ACTVT)
                Document type (BSART)

3. Authorization: An authorization object with specific field values assigned.

        Ex: Auth object: M_BEST_BSA
            Activity (ACTVT): 01,02,03
            Document type (BSART): NB(standard po)

4. Profile: A technical container generated from role authorization at the time of creation.
   - Generated when you click "Generated Profile" in PFCG.

         Ex: T-PD56999

5. Role: Central authorization objects of SAP.

        Contains: Menu
                  Transactions
                  Fiori Apps
                  Authorizations
        
        Types of roles:
                Single Roles
                Derived Roles
                Composite Roles
                Master Roles
                Technical Roles
                Business Roles

       Ex: Z_2329_MM_P01_MAINT_MASTER

6. Users: SAP Login account

Ex: PWIPRUK


#### Authorization checks at transaction start
    VA01 (Create Sales Order)
    |
    |----checks S_TCODE:TCD-'VA01'  ==NO==> "No Authorization to transaction VA01.
                |
                |
                YES--- Checks objects for VA01   ==NO==> 'missing authorization objects
                       (V_VBAK_VKO,ACTVT,SPART)  
                        |
                        | 
                        YES ==> Executes the ABAP Program and checks for next screen/program.


                        



