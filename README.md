# code_deploy

Simple code deploy application.

## Step 1: Create 2 IAM Roles

One for EC2 and one for EC2 to S3.

## Step 2: Create Instance

Get your instance ready to go and create a snapshot. Ensure you are the only one that can ssh by restricting IP address and whatnot.

## Step 3: Create New Application in CodeDeploy

For this application, it would be good to name `<AppName>` and create the following "Deployment Group Name"s:

- Testing
- Staging
- Production

Also, connect to GitHub.

## Step 4: Create an IAM Policy

Create a `CodeDeploy<AppName>` policy following the `aws/policy_template.json`.
  
## Step 5: Create a User and Attach the IAM Policy from Step 1

The user should probably be something like `GitHub<AppName>`. Store the AWS access key and secret access key in a safe place. If you lose them, you can always create new ones and expire the old ones.

## Step 6: Add AWS CodeDeploy to GitHub

Got to GitHub > "your project" > Settings > Integrations & services and add the configurations from above.

