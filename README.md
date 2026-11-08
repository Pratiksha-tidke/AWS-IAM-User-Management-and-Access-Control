# AWS-IAM-User-Management-and-Access-Control
"Hands-on implementation of AWS IAM User creation, access management, permission assignment, and security best practices using the Principle of Least Privilege."

## Table of Contents

* [Introduction](#introduction)
* [Objectives](#objectives)
* [IAM Architecture](#iam-architecture)
* [How It Works](#how-it-works)
* [Tools and Technologies](#tools-and-technologies)
* [System Requirements](#system-requirements)
* [Practical Implementation – Step by Step](#practical-implementation--step-by-step)
  * [Step 1: Login to AWS Management Console](#step-1-login-to-aws-management-console)
  * [Step 2: Additional Verification](#step-2-additional-verification)
  * [Step 3: AWS Management Console – Home Page](#step-3-aws-management-console--home-page)
  * [Step 4: AWS IAM – Identity and Access Management](#step-4-aws-iam--identity-and-access-management)
  * [Step 5: AWS IAM Dashboard](#step-5-aws-iam-dashboard)
  * [Step 6: AWS IAM – User Groups](#step-6-aws-iam--user-groups)
  * [Step 7: AWS IAM – Create User Group](#step-7-aws-iam--create-user-group)
  * [Step 8: AWS IAM – Attach Permissions Policies](#step-8-aws-iam--attach-permissions-policies)
  * [Step 9: AWS IAM – Attach Permission Policies](#step-9-aws-iam--attach-permission-policies)
  * [Step 10: AdministratorAccess Managed Policy](#step-10-administratoraccess-managed-policy)
  * [Step 11: AdministratorAccess Policy Permissions](#step-11-administratoraccess-policy-permissions)
  * [Step 12: Creating an IAM User Group](#step-12-creating-an-iam-user-group)
  * [Step 13: Admin IAM User Group Created](#step-13-admin-iam-user-group-created)
  * [Step 14: Creating an IAM User](#step-14-creating-an-iam-user)
  * [Step 15: IAM User Password Configuration](#step-15-iam-user-password-configuration)
  * [Step 16: Set Permissions](#step-16-set-permissions)
  * [Step 17: Adding User to a Group and Setting Permissions Boundary](#step-17-adding-user-to-a-group-and-setting-permissions-boundary)
  * [Step 18: Assigning Permissions to an IAM User](#step-18-assigning-permissions-to-an-iam-user)
  * [Step 19: Review and Create IAM User](#step-19-review-and-create-iam-user)
  * [Step 20: Add Tags (Optional)](#step-20-add-tags-optional)
  * [Step 21: IAM User Created Successfully](#step-21-iam-user-created-successfully)
  * [Step 22: IAM User Login Credentials](#step-22-iam-user-login-credentials)
  * [Step 23: AWS IAM User Login](#step-23-aws-iam-user-login)
  * [Step 24: IAM User Password Reset](#step-24-iam-user-password-reset)
  * [Step 25: IAM User Password Reset Successful](#step-25-iam-user-password-reset-successful)
  * [Step 26: AWS Management Console – Home Dashboard](#step-26-aws-management-console--home-dashboard)
  * [Step 27: AWS Console – IAM Service Search](#step-27-aws-console--iam-service-search)
  * [Step 28: AWS IAM Dashboard – Security Recommendations](#step-28-aws-iam-dashboard--security-recommendations)
  * [Step 29: AWS IAM – Assign MFA Device](#step-29-aws-iam--assign-mfa-device)
  * [Step 30: AWS IAM – MFA Authentication Methods](#step-30-aws-iam--mfa-authentication-methods)
  * [Step 31: AWS IAM – Scan MFA QR Code](#step-31-aws-iam--scan-mfa-qr-code)
  * [Step 32: AWS IAM – Security Credentials Page](#step-32-aws-iam--security-credentials-page)
  * [Step 33: AWS IAM – MFA Device Management](#step-33-aws-iam--mfa-device-management)
  * [Step 34: AWS IAM – Security Credentials Overview](#step-34-aws-iam--security-credentials-overview)
  * [Step 35: AWS Console – Account Menu](#step-35-aws-console--account-menu)
  * [Step 36: AWS Console – MFA Sign-In Verification](#step-36-aws-console--mfa-sign-in-verification)
  * [Step 37: AWS Management Console – Home Dashboard](#step-37-aws-management-console--home-dashboard)
  * [ Cloud Identity Protection & Security Guidelines](#Cloud-Identity-Protection-&-Security-Guidelines)
  * [ Disclaimer](#Disclaimer)


## Introduction

AWS Identity and Access Management (IAM) is a security service provided by Amazon Web Services (AWS). It helps administrators securely control access to AWS resources. IAM allows administrators to create users, groups, and roles and assign permissions through IAM policies.
An IAM User represents an identity within AWS that can be assigned specific permissions to access AWS services and resources.
Each IAM user can have:
- A username.
- Console access (optional).
- Access keys for programmatic access (optional).
- Permissions through IAM policies.
- Membership in IAM groups.

For example, an organization can create separate IAM users for developers, security analysts, and administrators, giving each user only the permissions required for their job.

## Objectives

The main objectives of this project are:
1. Understand **AWS Identity and Access Management (IAM)** and its role in cloud security.
2. Create and configure **IAM users.**
3. Understand **Authentication and Authorization.**
4. Assign permissions using **IAM Policies.**
5. Implement the **Principle of Least Privilege.**
6. Configure secure **AWS Console Access.**
7. Apply **IAM Security Best Practices.**
8. Manage and control user access to **AWS Resources.**
To gain hands-on experience in AWS IAM by creating users, managing permissions, configuring access controls, and securing access to AWS resources.

## IAM Architecture 

<img width="800" height="800" alt="IAM Pic" src="https://github.com/user-attachments/assets/899f2272-6649-423f-84f3-105bbbb44082" />


| Component | Explanation |
| --- | --- |
| **IAM User** | Represents a person or application that interacts with AWS. |
| **IAM Group** | A collection of IAM users used to specify permissions for multiple users at once. |
| **IAM Role** | An identity with specific permissions that can be assumed by trusted entities (users, services, or external identities). |
| **IAM Policy** | A document that defines allowed or denied actions on specific AWS resources. |
| **Authentication** | The process of verifying the identity of a user or service. |
| **Authorization** | The process of determining what actions and resources a verified identity can access. |
| **AWS Resources** | Services and infrastructure managed within AWS, such as EC2, S3, and RDS. |

## How it works:
1. The **administrator creates an IAM user.**
2. The user **authenticates using their credentials.**
3. AWS **evaluates the user's permissions.**
4. IAM policies determine which actions are **allowed or denied.**
5. The **user accesses only** the resources permitted by their effective permissions.

 ## Tools and Technologies
| Tool | Purpose |
| --- | --- |
| **AWS Management Console** | Manage AWS services |
| **AWS IAM** | Identity and access management |
| **IAM Users** | Create user identities |
| **IAM Groups** | Organize users |
| **IAM Policies** | Assign permissions |
| **Google Authenticator** | Generate MFA codes |
| **Web Browser** | Access AWS Console |

## System Requirements
- AWS account.
- Internet connection.
- Web browser (Chrome/Firefox).
- Valid email address.
- Authenticator application (for MFA).
- Basic understanding of cloud computing.

 ## Practical Implementation – Step by Step

#### Step 1: Login to AWS Management Console
1. Open the AWS Management Console.
2. Sign in using your AWS account.
3. Open the AWS Management Console.
   <img width="1324" height="569" alt="Screenshot 2026-10-11 152115" src="https://github.com/user-attachments/assets/e0ff6bf1-b9a5-4046-aded-5a9463cf1cdf" />

#### Step 2: Additional Verification  
1. AWS MFA provides an additional layer of security to user accounts.
2. It requires a 6-digit verification code from an authenticator app.
3. The user enters the code to verify their identity.
4. After successful verification, the user can securely access their AWS account.
<img width="1317" height="560" alt="Screenshot 2026-10-11 152218" src="https://github.com/user-attachments/assets/032ab776-39ec-4f5f-a937-1117c9000c8f" />

#### Step 3: AWS Management Console – Home Page
The AWS Management Console provides a centralized dashboard to manage AWS services, monitor resource health, and track cloud costs in one place.
<img width="1327" height="505" alt="Screenshot 2026-10-11 152353" src="https://github.com/user-attachments/assets/0777135a-4d24-42ec-903a-b331adef358d" />

#### Step 4: AWS IAM – Identity and Access Management
AWS IAM helps manage user identities, permissions, and secure access to AWS services and resources.

- *IAM:* Manages users, groups, roles, and permissions.
-  *IAM Identity Center:* Manages workforce access to multiple AWS accounts.
-  *MediaStore:* Stores and delivers media content.
<img width="1349" height="558" alt="Screenshot 2026-10-11 152442" src="https://github.com/user-attachments/assets/deaada43-0e93-4d5e-bd9f-16bad0e93d4c" />

#### Step 5: AWS IAM Dashboard
The AWS IAM Dashboard helps manage users, roles, and permissions while monitoring account security.

- *Root User MFA:* Enabled for extra security.
- *Access Keys:* No active root access keys.
- *IAM Roles:* 3 roles created.
- *Users & Groups:* No users or groups created.
- *Security Status:* Displays account security information.
 To manage access and protect AWS resources from unauthorized access.
<img width="1355" height="561" alt="5" src="https://github.com/user-attachments/assets/e2dd7694-4426-424e-888c-4dac24bd6e58" />

#### Step 6: AWS IAM – User Groups
The IAM User Groups page helps manage multiple users together.

- *User Groups:* No groups created yet.
- *Create Group:* Create a new user group.
- *Permissions:* Give permissions to multiple users.
 To manage users and their access easily.
<img width="1366" height="560" alt="6" src="https://github.com/user-attachments/assets/828f98ea-4ddc-4780-9443-6138163ed6b0" />

#### Step 7: AWS IAM – Create User Group
Allows you to create a new IAM user group.

- *Group Name:* Enter a name for the new group.
- *Add Users:* Add existing IAM users to the group.
- *Optional:* You can create a group without adding users.
 To organize users and manage their permissions together.
<img width="1354" height="563" alt="7" src="https://github.com/user-attachments/assets/14ecc5c5-0ace-48ea-a244-2e77138ab683" />

#### Step 8: AWS IAM – Attach Permissions Policies
Allows you to attach permission policies to a user group.

- *Policies:* Select policies to give permissions.
- *Permissions:* Control what users can access.
- *Account Management:* Manage account-related permissions.
 To control user access to AWS services and resources.
<img width="1348" height="555" alt="8" src="https://github.com/user-attachments/assets/fbd97810-9ea3-45e3-b6a0-10f30887b383" />

#### Step 9: AWS IAM – Attach Permission Policies
 Allows you to assign permissions to an IAM user group.
 
- *Administrator Access:* Provides full access to AWS services.
- *Permission Policies:* Control what users can access.
- *User Group:* Shares permissions with group members.
 To manage and control user access to AWS resources.
<img width="1366" height="556" alt="10" src="https://github.com/user-attachments/assets/2ef320a2-20e4-4634-9264-b72d854d45bc" />

#### Step 10: AdministratorAccess Managed Policy
The **AdministratorAccess** policy is an AWS-managed policy that provides full access to AWS services and resources. It allows users to manage and control AWS resources.

- **Policy Name:** AdministratorAccess
- **Policy Type:** AWS Managed
- **Permissions:** 476 (as displayed in the console)
- **Purpose:** Provides full administrative access.
Assign this policy only to trusted administrators. Follow the **Principle of Least Privilege** by giving users only the permissions they need.
<img width="1354" height="568" alt="11" src="https://github.com/user-attachments/assets/464b41f7-eb55-4d61-b775-c8e193b6c47b" />

#### Step 11:  AdministratorAccess Policy Permissions

The **AdministratorAccess** policy provides full access to all AWS services and resources. It allows administrators to manage AWS services and perform different actions across the account.
The console displays the service name, access level, resources, and request conditions for each permission.
<img width="1366" height="555" alt="12" src="https://github.com/user-attachments/assets/cdf3237d-9a0e-4d8f-b184-8d14e41267eb" />

#### Step 12: Creating an IAM User Group

An **IAM User Group** is a collection of IAM users managed together. It helps administrators manage permissions easily by assigning policies to a group instead of assigning permissions to each user individually.

- *Service:* AWS IAM
- *Purpose:* Group multiple IAM users.
- *Permissions:* Assign policies to the group.
- *Access:* Members receive group permissions.
- *Benefit:* Simplifies access management.
<img width="1366" height="565" alt="13" src="https://github.com/user-attachments/assets/c30de171-93c8-4afe-a45e-73f306c92b8e" />

#### Step 13: Admin IAM User Group Created
The Admin user group has been successfully created in the AWS IAM console. This group can be used to manage administrative permissions and assign IAM users.

- *Service:* AWS IAM
- *Group Name:* Admin
- *Users:* 0 users assigned
- *Purpose:* Manage administrative access and permissions.
- *Status:* Successfully created.
<img width="1366" height="565" alt="13" src="https://github.com/user-attachments/assets/2b9d33d8-1f0f-4f7c-991d-595e7c58c9a2" />

  #### Step 14: Creating an IAM User
The administrator to create a new IAM user by entering a username and configuring AWS Management Console access with an autogenerated or custom password.

- *Service:* AWS IAM
- *Action:* Create User
- *Username:* Enter a unique username.
- *Console Access:* Enable user login access.
- *Password:* Choose autogenerated or custom password.
  <img width="1366" height="568" alt="15" src="https://github.com/user-attachments/assets/33958fbe-3bbf-4015-b725-3408b7854cc2" />

#### Step 15: IAM User Password Configuration
The administrator to set a password for the IAM user using an autogenerated or custom password. The user can be required to change the temporary password during the first login.
- *Password Type:* Autogenerated or Custom.
- *Password Length:* Minimum 8 characters.
- *Password Security:* Follow AWS password requirements.
- *First Login:* User must change the temporary password.
<img width="1366" height="603" alt="33" src="https://github.com/user-attachments/assets/13df10fc-8be9-482a-898e-e5cc26503614" />

#### Step 16: (Step 2): Set Permissions

 Allows the administrator to assign permissions to a new IAM user. Permissions can be assigned by adding the user to an existing group, copying permissions from another user, or attaching policies directly. Adding users to groups is recommended because it makes permission management easier and more organized.
<img width="1366" height="566" alt="17" src="https://github.com/user-attachments/assets/2c84b933-937d-4a9f-85ea-bd67b1251e7a" />

### Step 17: Adding User to a Group and Setting Permissions Boundary

Allows the administrator to add the new IAM user to an existing group, such as **Admin**, so the user can inherit its permissions. An optional permissions boundary can also be configured to set the maximum permissions the user can have.
<img width="1354" height="565" alt="18" src="https://github.com/user-attachments/assets/6b5aef1d-8eef-4fa8-9481-d572ee1650f8" />

#### Step 18: Assigning Permissions to an IAM User

 The new IAM user is added to the **Admin group**, which has the AdministratorAccess policy attached. An optional permissions boundary can limit the maximum permissions available to the user. After assigning permissions, click **Next** to review the details before creating the user.
<img width="1366" height="555" alt="19" src="https://github.com/user-attachments/assets/383464b0-4459-48fb-b507-6c08816bea3a" />

#### Step 19: (Step 3): Review and Create IAM User

This step displays a summary of the new IAM user's details, assigned permissions, and password settings. Review all the information carefully before clicking **Create user** to complete the process.
<img width="1366" height="570" alt="20" src="https://github.com/user-attachments/assets/61da6832-ea43-4eb7-b6e0-ca066fe2a307" />

#### Step 20: (Step 4): Add Tags (Optional)

Allows the administrator to add tags to an IAM user using key-value pairs. Tags help organize and identify users. Adding tags is optional, so you can skip this step if they are not required and continue to create the user.
<img width="1366" height="567" alt="21" src="https://github.com/user-attachments/assets/cf37d500-3719-4c30-8b7b-e6f2679f4326" />

 #### Step 21:  IAM User Created Successfully
- IAM user creation completed successfully.
- AWS console sign-in URL generated.
- Username and temporary password provided.
- Login details can be downloaded as a CSV file.
- Password must be saved securely for future login.
  <img width="1366" height="564" alt="22" src="https://github.com/user-attachments/assets/caedadea-7cfa-4142-9a81-15a6abd306d3" />

#### Step 22: IAM User Login Credentials
This section displays the newly created IAM user's login details, including the AWS sign-in URL, username, and temporary password. The credentials can be viewed or copied and should be stored securely for future access.
<img width="1366" height="561" alt="23" src="https://github.com/user-attachments/assets/89140b88-bdb7-4d66-adf1-977747273b72" />

#### Step 23: AWS IAM User Login
This page allows users to access the AWS Management Console using their assigned account ID, IAM username, and password.
- *Account ID/Alias:* Identifies the AWS account.
- *IAM Username:* Identifies the user.
- *Password:* Authenticates the user.
- *Root User Login:* Allows the account owner to sign in using their registered email address.
<img width="1339" height="476" alt="24" src="https://github.com/user-attachments/assets/aa50a662-1f00-4b19-9174-89886802800a" />

#### Step 24: IAM User Password Reset
This page allows IAM users to change their temporary or expired password and create a new password before accessing the AWS Management Console.
- *Old Password:* Enter the current password.
- *New Password:* Create a strong password.
- *Confirm Password:* Re-enter the new password.
- *Update:* Click the confirmation button to save the new password.
- *Sign in to a Different Account:* Switch to another AWS account if needed.
  <img width="1332" height="622" alt="25" src="https://github.com/user-attachments/assets/5b8442c6-6e1d-4bbc-9b40-5e42065fdf20" />

#### Step 25: IAM User Password Reset Successful
The IAM user's password has been successfully updated. The user can now continue to the AWS Management Console using the new password.
- Password reset completed successfully.
- Click Continue to proceed with sign-in.
- Use the new password to log in.
- Complete MFA verification if enabled.
  <img width="1195" height="470" alt="26" src="https://github.com/user-attachments/assets/f57531de-f83e-41dc-bd0c-60a357c78e47" />

#### Step 26: AWS Management Console – Home Dashboard
The AWS Management Console provides a centralized interface to access and manage AWS services.
- *Top Navigation Bar:* Access AWS search, CloudShell, notifications, and account settings.
- *Recently Visited Services:* Quick access to EC2, S3, CloudWatch, and IAM.
- *Welcome to AWS:* Provides learning and training resources.
- *AWS Health:* Displays service health and account notifications.
- *Dashboard Controls:* Allows users to customize the dashboard using widgets.
  <img width="1366" height="601" alt="27" src="https://github.com/user-attachments/assets/17ffa908-560b-4f43-a80c-131a1fa4a184" />

  #### Step 27: AWS Console – IAM Service Search
 AWS search results for Identity and Access Management (IAM).
Key Services:
- *IAM:* Manages users, groups, roles, and permissions.
- *IAM Identity Center:* Manages workforce access across multiple AWS accounts.
- *Resource Access Manager:* Shares AWS resources across accounts.
- *IAM Access Analyzer:* Identifies unintended access and analyzes permissions.
 <img width="1351" height="602" alt="28" src="https://github.com/user-attachments/assets/dc3b706d-d7d3-452e-b74b-b9954eef84f2" />

  #### Step 28: AWS IAM Dashboard – Security Recommendations

The AWS IAM Dashboard, highlighting security recommendations and IAM resource information.

Key Components:
- *Security Recommendations:* Displays MFA security recommendations for account protection.
- *IAM Resources:* Shows the total number of users, groups, roles, policies, and identity providers.
- *MFA Configuration:* Provides options to enable Multi-Factor Authentication for additional security.
- *Quick Links:* Offers access to security credentials, MFA settings, and account aliases.
<img width="1366" height="600" alt="29" src="https://github.com/user-attachments/assets/885227ac-1701-473b-bccd-4b33bfc8db02" />

#### Step 29: AWS IAM – Assign MFA Device
1. *Device Name:* Enter a recognizable name, e.g., Google-Authenticator.
2. *MFA Device Type:* Select your preferred authentication method:
   - Authenticator App: Google Authenticator, Authy, or Microsoft Authenticator.
   - Passkey/Security Key: Uses biometric authentication or a hardware security key.
3. *Next:* Click Next to proceed with MFA device registration.
<img width="1366" height="602" alt="30" src="https://github.com/user-attachments/assets/d8b7308c-4bce-4c1d-b64b-6962c8dbc412" />

#### Step 30: AWS IAM – MFA Authentication Methods
1. *Passkey/Security Key:* Uses fingerprint, face recognition, or a security key.
2. *Authenticator App:* Generates verification codes through an authentication app.
3. *Hardware TOTP Token:* Generates codes using a physical device.
Next: Select a method and click Next to complete MFA setup.
<img width="1366" height="603" alt="31" src="https://github.com/user-attachments/assets/f8375221-83a7-40f4-a417-5a4f3bb8270c" />

#### Step 31: AWS IAM – Scan MFA QR Code
1. Open Google Authenticator or Microsoft Authenticator.
2. Select Add Account and scan the AWS QR code.
3. Enter two consecutive 6-digit verification codes in AWS.
4. Click Add MFA to complete device registration.
<img width="1366" height="599" alt="34" src="https://github.com/user-attachments/assets/337af3a7-ccd8-4c09-b5c5-6d8949a9e33f" />

#### Step 32: AWS IAM – Security Credentials Page
Displays account information and security credential settings.
1. *Navigation Pane:* Access IAM users, groups, roles, and policies.
2. *MFA Status:* Shows MFA device configuration.
3. *Account Details:* Displays username, Account ID, and User ARN.
4. *IAM Credentials:* Manages account security credentials.
5. *Access Keys:* Manages API access keys.
6. *Other Credentials:* Includes CodeCommit and Amazon Keyspaces credentials.
   <img width="1366" height="604" alt="35" src="https://github.com/user-attachments/assets/1b52e2f5-9312-44c5-be20-be2afa0c5e26" />


#### Step 33: AWS IAM – MFA Device Management

The screenshot shows an assigned MFA device under AWS IAM Security Credentials.

1. *MFA Status:* Device successfully assigned.
2. *Device ID:* Displays the assigned MFA device ID.
3. *Available Actions:* Remove, Resync, or Assign MFA device.
4. *Console Sign-in:* Displays password status and last sign-in time.

<img width="1366" height="601" alt="36" src="https://github.com/user-attachments/assets/9c69011d-8d82-4dd0-a0e8-e5c322543a3b" />

### Step 34: AWS IAM – Security Credentials Overview

 The AWS IAM Security Credentials page, displaying the account's security configuration. One virtual MFA device is successfully assigned, while no access keys or X.509 certificates are currently configured. It also provides options to manage MFA devices and security credentials.
 <img width="1366" height="603" alt="37" src="https://github.com/user-attachments/assets/8e506f6d-59b1-46d8-8d1d-6f48c1330b10" />

#### Step 35: AWS Console – Account Menu

 The AWS account menu, providing account information, management options, and session controls.
1. *Account Details:* Displays Account ID, account name, and IAM username.
2. *Management & Billing:* Provides access to billing, service quotas, and security credentials.
3. *Multi-Session Support:* Allows multiple AWS sessions.
4. *Switch Role:* Enables access through a different IAM role.
5. *Sign Out:* Securely ends the current AWS session.
   <img width="1366" height="603" alt="39" src="https://github.com/user-attachments/assets/16897549-5de0-4fc2-ba26-0f808a264fb1" />


 #### Step 36: WS Console – MFA Sign-In Verification
 The AWS sign-in page requesting a 6-digit MFA verification code.
1. MFA Code: Enter the 6-digit code from your authenticator app.
2. Sign In: Click the Sign In button to complete authentication and access the AWS Console.

 <img width="1340" height="614" alt="40" src="https://github.com/user-attachments/assets/6385a654-8b74-4fbd-8429-86aebc357305" />

#### Step 37: AWS Management Console – Home Dashboard
The AWS Management Console acts as a central control panel for managing cloud resources, monitoring services, and configuring AWS infrastructure.

<img width="1350" height="593" alt="41" src="https://github.com/user-attachments/assets/94fc7975-af99-4fd4-9b5f-4d02224af682" />

## Cloud Identity Protection & Security Guidelines

1. **Protect the Root Account:** Do not use the AWS root account for daily activities. Use a separate IAM administrator account for regular management tasks.
2. **Use Administrator Permissions Carefully:** Assign AdministratorAccess only to trusted users who require full administrative permissions. Avoid giving unnecessary permissions to other users.
3. **Follow Least Privilege:** Give each user only the permissions required to perform their assigned tasks.
4. **Secure User Credentials:** Require users to change their initial passwords and never share passwords or access keys.
5. **Enable MFA:** Enable Multi-Factor Authentication (MFA) for the root account and administrator accounts to add an extra layer of security.
6. **Manage Group Permissions:** Use IAM groups to manage permissions centrally. Remove users from groups when they no longer require access.

##### *These security practices help reduce unauthorized access, protect AWS accounts, and improve cloud security.*
----

## Disclaimer

This project is created for educational purposes and hands-on AWS cloud security learning. It demonstrates IAM user management, access control, permission management, and MFA configuration.
All activities should be performed only in authorized AWS environments. Never share or upload passwords, access keys, secret keys, or MFA QR codes publicly.
The project follows basic cloud security practices, including the Principle of Least Privilege and secure credential management.
The author is not responsible for any misuse or unauthorized activities involving this project.
This is an independent educational project and is not affiliated with or endorsed by Amazon Web Services (AWS).
