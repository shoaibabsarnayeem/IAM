## EXPERIMENT NO : 6

## Login into AWS and Implement Identity Management Using Amazon IAM

## Name : Shoaib absar nayeem

## Reg No : 212225040408

## Aim

To create and configure IAM users and groups in AWS, assign permissions using IAM policies, enable console access, and verify role-based access to Amazon S3.

## Requirements

1. AWS Account
2. Internet connection
3. Web browser
4. Amazon S3 bucket

## Procedure

## Step 1: Login to AWS Management Console

1. Open a web browser.
2. Go to the AWS Management Console.
3. Sign in using the AWS account credentials.
4. Search for IAM using the AWS search bar.
5. Open IAM (Identity and Access Management).

## Step 2: Create an IAM Group

1. In the IAM dashboard, select User groups from the left-side menu.

2. Click Create group.

3. Enter the group name:

cloudSecurity_2026

4. Do not add users at this stage if the user will be created separately.

5. Click Create user group.

The group cloudSecurity_2026 is now created.

## Step 3: Attach an IAM Policy to the Group

1. Open the cloudSecurity_2026 group.

2. Select the Permissions tab.

3. Click Add permissions.

4. Select Attach policies directly.

5. Search for:

AmazonS3ReadOnlyAccess

6. Select the checkbox for AmazonS3ReadOnlyAccess.

7. Click Next and then Add permissions.

The group now has read-only access to Amazon S3.

## Step 4: Create an IAM User

1. From the IAM navigation menu, select Users.

2. Click Create user.

3. Enter the username:

student01

4. Click Next.

## Step 5: Add the User to the IAM Group

1. On the Permissions page, select Add user to group.

2. Select:

cloudSecurity_2026

3. Click Next.

4. Review the configuration.

5. Click Create user.

The user is now a member of the cloudSecurity_2026 group.

## Step 6: Verify User Permissions

1. Open IAM → Users.

2. Click student01.

3. Open the Permissions tab.

4. Verify that the following policy is displayed:

AmazonS3ReadOnlyAccess

5. Check the Attached via column.

6. It should indicate that the policy is attached through:

Group: cloudSecurity_2026

This demonstrates:

student01 → cloudSecurity_2026 → AmazonS3ReadOnlyAccess → Amazon S3 Read-only Access

## Step 7: Enable Console Access

Initially, console access for student01 may be disabled.

1. Open IAM → Users → student01.
2. Select Security credentials.
3. Locate Console access / AWS Management Console access.
4. Enable console access.
5. Create a console password for student01.
6. Complete the configuration.

## Note: Do not share the password with other users.

## Step 8: Obtain the AWS Account ID

The IAM user login requires the AWS account ID.

1. The AWS account ID is a 12-digit number.

2. It can be found in the AWS account information.

3. For the demonstration account used in this experiment, the account ID was:

018673110217

Students should use their own AWS account ID when performing the experiment.

## Step 9: Login as the IAM User

1. Sign out from the current AWS administrator/root session.

2. Open a new browser window or Incognito/Private window.

3. Open the AWS sign-in page.

4. Select IAM user login.

5. Enter the AWS account ID.

6. Enter the IAM username:

student01

7. Enter the password created in Step 7.

8. Click Sign in.

The AWS Management Console should now open under the IAM user student01.

## Step 10: Verify Amazon S3 Access

1. After logging in as student01, search for S3.
2. Open Amazon S3.
3. Select General purpose buckets.
4. Verify that the previously created S3 bucket is visible.
5. Open the bucket.
6. Verify that the user can view the bucket and its objects.
7. 
This confirms that the IAM policy is providing S3 read access.

## Step 11: Verify Least-Privilege Access

The user student01 has been assigned:

## AmazonS3ReadOnlyAccess

Therefore, the user should have read access but should not have permission to perform S3 write/delete operations.

For testing:

1. Open the S3 bucket as student01.
2. Observe the available operations.
3. Do not delete any existing object.
4. If you test an upload operation, do not use an important file.
5. The actual permission check occurs when AWS attempts the S3 operation.
6. A read-only user should receive an Access Denied response for unauthorized write/delete operations.

## Important: The S3 console may display an Upload button even when the user does not have permission to complete the upload. The presence of the button alone does not prove that upload permission exists.

## Screenshots

## 1. IAM User Groups

Add the screenshot showing the created IAM groups.

## 2. S3 Read-Only Policy

Add the screenshot showing AmazonS3ReadOnlyAccess attached to cloudSecurity_2026.

## 3. IAM Users

Add the screenshot showing the created IAM users, including student01.

## 4. User Permissions

Add the screenshot showing student01 with AmazonS3ReadOnlyAccess attached through cloudSecurity_2026.

## 5. MFA

Add the screenshot showing that MFA is enabled for the IAM user.

## 6. IAM Access Analyzer

Add the screenshot showing the successfully created Access Analyzer.

## 7. CloudTrail

Add the screenshot showing the CreateUser event in CloudTrail Event History.

## 8. Amazon S3 Access

Add the screenshot showing student01 accessing the S3 bucket and viewing its objects.

## Expected Result

The IAM group cloudSecurity_2026 is successfully created and assigned the AmazonS3ReadOnlyAccess policy. The IAM user student01 is successfully created, added to the group, and provided with AWS Management Console access. The user can log in to AWS and access the assigned S3 resources according to the permissions inherited from the group.
## EXPERIMENT NO : 6

## Login into AWS and Implement Identity Management Using Amazon IAM

## Name : DHILSANRAJ S

## Reg No : 212225230058

## Aim

To create and configure IAM users and groups in AWS, assign permissions using IAM policies, enable console access, and verify role-based access to Amazon S3.

## Requirements

1. AWS Account
2. Internet connection
3. Web browser
4. Amazon S3 bucket

## Procedure

## Step 1: Login to AWS Management Console

1. Open a web browser.
2. Go to the AWS Management Console.
3. Sign in using the AWS account credentials.
4. Search for IAM using the AWS search bar.
5. Open IAM (Identity and Access Management).

## Step 2: Create an IAM Group

1. In the IAM dashboard, select User groups from the left-side menu.

2. Click Create group.

3. Enter the group name:

cloudSecurity_2026

4. Do not add users at this stage if the user will be created separately.

5. Click Create user group.

The group cloudSecurity_2026 is now created.

## Step 3: Attach an IAM Policy to the Group

1. Open the cloudSecurity_2026 group.

2. Select the Permissions tab.

3. Click Add permissions.

4. Select Attach policies directly.

5. Search for:

AmazonS3ReadOnlyAccess

6. Select the checkbox for AmazonS3ReadOnlyAccess.

7. Click Next and then Add permissions.

The group now has read-only access to Amazon S3.

## Step 4: Create an IAM User

1. From the IAM navigation menu, select Users.

2. Click Create user.

3. Enter the username:

student01

4. Click Next.

## Step 5: Add the User to the IAM Group

1. On the Permissions page, select Add user to group.

2. Select:

cloudSecurity_2026

3. Click Next.

4. Review the configuration.

5. Click Create user.

The user is now a member of the cloudSecurity_2026 group.

## Step 6: Verify User Permissions

1. Open IAM → Users.

2. Click student01.

3. Open the Permissions tab.

4. Verify that the following policy is displayed:

AmazonS3ReadOnlyAccess

5. Check the Attached via column.

6. It should indicate that the policy is attached through:

Group: cloudSecurity_2026

This demonstrates:

student01 → cloudSecurity_2026 → AmazonS3ReadOnlyAccess → Amazon S3 Read-only Access

## Step 7: Enable Console Access

Initially, console access for student01 may be disabled.

1. Open IAM → Users → student01.
2. Select Security credentials.
3. Locate Console access / AWS Management Console access.
4. Enable console access.
5. Create a console password for student01.
6. Complete the configuration.

## Note: Do not share the password with other users.

## Step 8: Obtain the AWS Account ID

The IAM user login requires the AWS account ID.

1. The AWS account ID is a 12-digit number.

2. It can be found in the AWS account information.

3. For the demonstration account used in this experiment, the account ID was:

018673110217

Students should use their own AWS account ID when performing the experiment.

## Step 9: Login as the IAM User

1. Sign out from the current AWS administrator/root session.

2. Open a new browser window or Incognito/Private window.

3. Open the AWS sign-in page.

4. Select IAM user login.

5. Enter the AWS account ID.

6. Enter the IAM username:

student01

7. Enter the password created in Step 7.

8. Click Sign in.

The AWS Management Console should now open under the IAM user student01.

## Step 10: Verify Amazon S3 Access

1. After logging in as student01, search for S3.
2. Open Amazon S3.
3. Select General purpose buckets.
4. Verify that the previously created S3 bucket is visible.
5. Open the bucket.
6. Verify that the user can view the bucket and its objects.
7. 
This confirms that the IAM policy is providing S3 read access.

## Step 11: Verify Least-Privilege Access

The user student01 has been assigned:

## AmazonS3ReadOnlyAccess

Therefore, the user should have read access but should not have permission to perform S3 write/delete operations.

For testing:

1. Open the S3 bucket as student01.
2. Observe the available operations.
3. Do not delete any existing object.
4. If you test an upload operation, do not use an important file.
5. The actual permission check occurs when AWS attempts the S3 operation.
6. A read-only user should receive an Access Denied response for unauthorized write/delete operations.

## Important: The S3 console may display an Upload button even when the user does not have permission to complete the upload. The presence of the button alone does not prove that upload permission exists.

## Screenshots

## 1. IAM User Groups

Add the screenshot showing the created IAM groups.

## 2. S3 Read-Only Policy

Add the screenshot showing AmazonS3ReadOnlyAccess attached to cloudSecurity_2026.

## 3. IAM Users

Add the screenshot showing the created IAM users, including student01.

## 4. User Permissions

Add the screenshot showing student01 with AmazonS3ReadOnlyAccess attached through cloudSecurity_2026.

## 5. MFA

Add the screenshot showing that MFA is enabled for the IAM user.

## 6. IAM Access Analyzer

Add the screenshot showing the successfully created Access Analyzer.

## 7. CloudTrail

Add the screenshot showing the CreateUser event in CloudTrail Event History.

## 8. Amazon S3 Access

Add the screenshot showing student01 accessing the S3 bucket and viewing its objects.

## Expected Result

The IAM group cloudSecurity_2026 is successfully created and assigned the AmazonS3ReadOnlyAccess policy. The IAM user student01 is successfully created, added to the group, and provided with AWS Management Console access. The user can log in to AWS and access the assigned S3 resources according to the permissions inherited from the group.
<img width="1757" height="781" alt="image" src="https://github.com/user-attachments/assets/3a7c8e18-2205-441b-94cf-cb7cd5f8b156" />

<img width="1864" height="793" alt="image" src="https://github.com/user-attachments/assets/79bb8725-a335-4da5-95cc-9e884906f6c9" />

<img width="1805" height="783" alt="image" src="https://github.com/user-attachments/assets/8f3ee083-b017-4a29-a8d1-3bf771b529a0" />

<img width="1817" height="775" alt="image" src="https://github.com/user-attachments/assets/e97d80fa-fc68-478a-a1f8-9917f376dd49" />

## Result

Thus, Identity and Access Management (IAM) was successfully implemented in AWS by creating an IAM group, assigning an S3 read-only policy, creating an IAM user, enabling console access, and verifying permission-based access to Amazon S3.
