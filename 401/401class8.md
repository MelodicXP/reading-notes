# 401 - Class 08 - Access Control

## Why This Topic Matters  

  Role-Based Access Control (RBAC) is a critical component of managing user permissions and access control within any organization.

## 5 Steps to RBAC (Role Based Access Control)

1. **What is Role Based Access Control (RBAC) and why do we care?**  
    Role-Based Access Control (RBAC) is a method of regulating access to computer or network resources based on the roles of individual users within an organization.

    For example, RBAC lets employees have access rights only to the information they need to do their jobs and prevents them from accessing information that doesn't pertain to them. This approach to access control is particularly useful in organizations with diverse user communities and varying levels of confidentiality and security requirements.

    Why we care about RBAC:

    **Security Enhancement:** By implementing RBAC, organizations can significantly enhance their security posture. It ensures that users don't have excessive permissions that exceed their job requirements, thereby reducing the risk of malicious access or accidental data breaches.

    **Principle of Least Privilege:** RBAC enforces the principle of least privilege, ensuring that individuals have access only to the resources and information necessary for their duties. This minimization of access rights helps protect sensitive information and systems.

    **Efficiency and Scalability:** RBAC systems simplify the management of user permissions. Instead of assigning permissions to each user individually, administrators can assign roles based on job functions. As a result, managing and auditing permissions becomes more efficient, especially in large and growing organizations.

    **Compliance and Auditability:** Many regulatory frameworks require strict control over access to information. RBAC helps organizations comply with these regulations by providing a clear framework for access control and an easier way to demonstrate that access policies are being followed.

    **Operational Flexibility:** Roles can be easily modified, and users can be reassigned different roles as their job functions change within an organization. This flexibility ensures that access rights remain aligned with users' current needs and responsibilities.

    In summary, RBAC is a critical component of an organization's security strategy because it provides a structured and efficient method of managing user access to resources, enhancing security, and meeting compliance requirements.

2. **Describe a Role/Permission heirarchy that you might implement using RBAC**  

    **Implementing a Role/Permission Hierarchy with RBAC:** Implementing a Role/Permission hierarchy using RBAC involves defining a structured system where roles are associated with specific permissions, and users are assigned to these roles based on their job functions. This structure ensures that users have access only to the resources necessary for their roles, adhering to the principle of least privilege.

    **Basic Structure:**

    - **Roles**: Defined job functions within the organization, each with specific access rights.
    - **Permissions**: Specific actions or access levels that can be assigned to roles.

    **Example Hierarchy:**
      - **Visitor**
        - Permissions: Access public content, view product listings.
      - **Employee**
        - Inherits permissions from: Visitor.
        - Additional Permissions: Access to internal communication tools, time reporting system, and internal documentation.

      - **Manager:**
        - Inherits permissions from: Employee.
        - Additional Permissions: Access to performance reports of their team, project management tools, and budgeting tools.

      - **HR Manager:**
        - Inherits permissions from: Manager.
        - Additional Permissions: Access to all employee records, payroll system, and recruitment tools.

      - **IT Admin:**
        - Special Permissions: Full access to all IT systems, including creating and managing user accounts, setting up permissions, managing network security protocols, and access to all logs and monitoring tools.

      - **CEO:**
        - Inherits permissions from: Manager, but with broader access.
        - Special Permissions: Access to all business reports, financial data, strategic planning tools, and the ability to modify any user’s roles and permissions within the RBAC system.

    This RBAC hierarchy is scalable and can be adapted as the organization grows or as roles evolve. The key is maintaining a clear structure where each role has defined permissions that correspond to the responsibilities of the users in that role, thereby ensuring security and efficiency in accessing resources.

3. **What approach might you take to implement RBAC?**  
    1. **Identify Resources**  
    Start by identifying all the resources that need protection. Resources can include systems, applications, files, databases, and more. Understanding what needs to be protected is crucial for defining access levels.

    2. **Define Roles**  
    Analyze job functions within your organization to define roles. Roles should be based on the responsibilities and duties of the job functions rather than the individuals themselves. For example, roles could include Administrator, Manager, Editor, Viewer, etc.

    3. **Assign Permissions to Roles**  
    For each role, define the permissions that are necessary to perform its associated job functions. Permissions should be as granular as possible and can include actions such as read, write, delete, and execute. Make sure that permissions adhere to the principle of least privilege, giving each role only the access necessary to perform its tasks.

    4. **Create a Role-Permission Matrix**  
    To organize roles and their corresponding permissions, create a matrix or a list that maps each role to its permissions. This documentation will be instrumental in implementing and maintaining the RBAC system.

    5. **Assign Users to Roles**  
    Once roles and permissions are clearly defined, assign users to roles based on their job functions. Users can have multiple roles if their job functions require them to have varied access rights.

    6. **Implement Access Control Mechanisms**  
    Use the role-permission matrix to implement access control mechanisms in your IT environment. This may involve configuring your systems, applications, and network devices to enforce the defined roles and permissions.

    7. **Regularly Review and Update**  
    RBAC systems require regular review and updates to remain effective. As roles, permissions, and user assignments change, the RBAC system should be updated to reflect these changes. Conduct periodic audits to ensure compliance with policies and to identify any unnecessary permissions that could be removed.

## wiki - RBAC

1. **If Authentication is “you are who you say you are,” what is Authorization?**  
    Authorization is "you are allowed to do what you're trying to do." Authorization determines the resources and operations that an authenticated user is permitted to access or perform, based on their roles and the permissions associated with those roles.

2. **Name three primary rules defined for RBAC.**
    1. **Role assignment:** A subject can exercise a permission only if the subject has selected or been assigned a role.

    2. **Role authorization:** A subject's active role must be authorized for the subject. With rule 1 above, this rule ensures that users can take on only roles for which they are authorized.

    3. **Permission authorization:** A subject can exercise a permission only if the permission is authorized for the subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which they are authorized.
  
3. **Describe RBAC to a non-technical friend.**
    Imagine you're at a music festival with different areas, like the main stage, VIP lounge, and backstage. When you enter, you get a wristband. Think of this wristband as your "authentication" - it proves you bought a ticket.

    Now, RBAC is like different colored wristbands that determine where you can go in the festival. If you have a green wristband (a "role"), you can enter the VIP lounge because your wristband (role) has the permission to enter. If you have a blue wristband, maybe you can only go to the main stage area. The color of your wristband (your role) decides what areas (resources) you can access and what you can do (permissions) in the festival. This way, only people with the right wristband colors (roles) can access certain areas or perks, keeping things organized and secure.

## RBAC Tutorial

1. **What Are access rights Associated with? The User? or The Role? Explain.**
    Access rights are associated with the role, not directly with the user. Users are assigned a role, and each role has rights to access or perform certain functions.
    1. **Roles Represent Job Functions:** In RBAC, roles are created to represent job functions within an organization. Each role is assigned specific access rights that correspond to the job function's needs.

    2. **Users Are Assigned to Roles:** Users are then assigned to these roles based on their job functions. By associating access rights with roles rather than directly with users, managing and updating access becomes much simpler and more scalable.

2. **Access Rights, or Authorization, is activated after a user successfully does what?**  
    Authenticate themselves to the system.  User can then activate one or more roles for themselves.

    Access rights, or authorization, is activated after a user successfully authenticates themselves. In the process of accessing a system or application, authentication comes first, where the user proves their identity, typically through a username and password, biometrics, or other methods. Once the system verifies the user's identity, it then determines what the user is authorized to do based on their roles and permissions. This is the stage where access rights are applied, allowing or restricting actions within the system according to the user's authorized roles.

3. **Explain how RBAC might benefit a business.**  
    - Policy need not be udpated when a certain person with a role leaves organization.
    - New employee should be able to activate the desired role.
    - Principle of least privelege.  RBAC enforces the principle of least privilege, ensuring that users have the minimum level of access required to perform their jobs. This minimizes the risk surface and helps in maintaining a secure and efficient working environment.
    - User in one role has access to a subset of files.
    - Switch roles to gain access to other resources
    - SELinux supports RBAC

## Links to resources used for these notes

- [5 steps to RBAC](https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html)
- [wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)
- [RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)
- Chat GPT
