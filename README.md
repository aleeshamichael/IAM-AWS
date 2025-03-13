# IAM-AWS
# AWS Identity and Access Management (IAM)

## Introduction
AWS Identity and Access Management (IAM) helps control who can do what in your Amazon Web Services (AWS) account. This guide covers IAM basics such as managing users, groups, and policies, and understanding the difference between the root user and regular users.

## Getting Started with IAM
To use the IAM service in AWS:
1. Open the AWS Management Console.
2. In the search box, type `IAM` and select the IAM service.

## Creating Your First IAM User
1. Navigate to the IAM service in the AWS console.
2. Select `Users` from the navigation pane and click `Add Users`.
3. Enter a username (e.g., `TestUser`).
4. Check `Provide user access to the AWS Management Console (optional)` and select `I want to create an IAM user`.
5. Set a custom password.
6. On the `Set permissions` page, choose to either add the user to a group or attach policies directly.
7. Review and create the user.
8. Download the `.csv` file with credentials for future reference.

## Creating an IAM User Group
1. Navigate to `User Groups` and select `Create group`.
2. Enter a group name.
3. Select users to add to the group.
4. Choose policies to attach to the group.
5. Click `Create group`.

## Creating an IAM Policy
1. Go to `Policies` in the IAM navigation pane.
2. Click `Create policy`.
3. Choose between `Visual` and `JSON` editors.
4. Select a service (e.g., EC2) and specify actions (Allow/Deny).
5. Define resource access.
6. Provide a policy name and description.
7. Click `Create policy`.

## Creating an IAM Role
1. Navigate to `Roles` and select `Create role`.
2. Choose the AWS account or service requiring the role.
3. Select policies to attach.
4. Provide a role name and description.
5. Click `Create role`.

## IAM Programmatic Access
Programmatic access allows interaction with AWS services via API or CLI:
1. Navigate to the `Users` section in IAM.
2. Select or create a user with `Programmatic Access` enabled.
3. Attach necessary permissions.
4. Download the access key `.csv` file.

## AWS CLI Setup
1. Install AWS CLI from the [official documentation](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).
2. Verify installation with:
   ```sh
   aws --version
   ```
3. Configure credentials:
   ```sh
   aws configure
   ```
4. Test setup:
   ```sh
   aws s3 ls
   aws ec2 describe-instances
   ```

## Conclusion
IAM allows for secure access management in AWS by defining user roles, policies, and permissions. Following best practices, such as least privilege access, ensures a secure AWS environment.

## References
- [AWS IAM Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
