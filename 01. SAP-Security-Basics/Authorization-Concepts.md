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




