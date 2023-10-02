# Users are very important in IAM you have a root user which is the first user created when you setup your AWS account
- Root user has complete admin access
- You can create more users and give them different permissions
- You can create groups and assign users to groups
- You can use "Policies" to assign permissions to users
- You can use "Roles" to assign permissions to AWS resources
- IAM is universal, does not apply to regions at this time
- The "root account" is simply the account created when first setup your AWS account. It has complete Admin access
- New Users have NO permissions when first created
- New Users are assigned Access Key ID & Secret Access Keys when first created
- These are not the same as a password, and you cannot use the Access Key ID & Secret Access Key to Login in to the console. You can use this to access AWS via the APIs and Command Line however.
- You only get to view these once. If you lose them, you have to regenerate them

# MFA (Multi Factor Authentication) how to protect users and groups 
- You should protect your root user and IAM users with MFA
- MFA = password you know + security device you own
- MFA devices 
    - Virtual MFA device (Google Authenticator, Authy 2-Factor Authentication)
    - Universal 2nd Factor (U2F) security key (YubiKey by Yubico)
    - Hardware Key Fob MFA Device (Gemalto)
    - Hardware MFA Key Fob Device for AWS GovCloud (US) (SurepassID)

# AWS CLI & SDK
- AWS CLI = Command Line Interface / alternative to using the console
- SDK = Software Development Kit /language specific APIs enables you to also interact with AWS via code embbed within your application
- Mobile SDK's & Iot SDK's are also available
## Note:
    - You can use cloud shell to run AWS CLI commands and you have a whole directory to work with you can upload and download files which could be useful 

# IAM Roles
- Its like permissions for AWS services rather than users
- you can assign roles to AWS resources
- Example: EC2 instances, Lambda functions, CloudFormation, etc

# IAM Security Tools
- IAM Credentials report (Account level)
    - List all your account users and the status of their various credentials
- IAM Access Advisor (User level)
    - Shows service permissions granted to a user and when those services were last accessed