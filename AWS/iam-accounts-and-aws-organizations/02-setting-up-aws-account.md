# A Comprehensive Guide on Getting Started with AWS: Account Setup, CLI Configuration, and Managing Credentials


Amazon Web Services (AWS) is one of the leading cloud computing platforms, offering a vast array of services that enable individuals and businesses to host websites, store data, and run applications with flexibility and scalability. However, before diving into the myriad of services AWS offers, it's essential to start with setting up an account and understanding how to explore the platform using AWS’s Free Tier. This guide will walk you through the process of setting up an AWS account, as well as how to make the most of the Free Tier for learning purposes.

## Step 1: Setting Up Your AWS Account

###  Create an AWS Account
The first step is to visit the AWS homepage and click on “Create a Free Account.” If you already have an Amazon account (used for shopping), you can use that to sign up for AWS. Otherwise, you’ll need to create a new account.

#### Basic Account Setup:
- **Email Address**: You’ll need to provide a valid email address, which will be used to manage your AWS account.
- **Password**: Create a secure password for your AWS account.
- **Account Name**: Choose an account name that suits your needs (e.g., personal or business).

### Identity Verification
AWS requires you to verify your identity. This is done by entering your contact information, including your phone number. AWS will then send you an automated call or text message to verify that you’re a real person.

### Payment Information
Although AWS offers a Free Tier, you still need to provide valid payment information. AWS uses your credit card or debit card to confirm your identity. However, don’t worry about being charged for using the Free Tier, as it comes with specific usage limits that won't exceed the free allowance unless you opt for paid services.

### Select a Support Plan
At this stage, AWS will ask you to choose a support plan. For beginners, the “Basic Support Plan” is sufficient. This plan is free of charge and includes 24/7 access to customer service and documentation, but it doesn't offer technical support.

### Agree to Terms and Complete Registration
After providing all the necessary information, you’ll need to review and agree to AWS’s terms and conditions. Once completed, you’ll be able to access the AWS Management Console, the primary interface for managing your AWS resources.

## Accessing the AWS Management Console
Once your account is set up, you can log in to the AWS Management Console. This is where you will access and manage all of your AWS services. The console is user-friendly and allows you to manage everything from compute resources to storage and databases. You will see a navigation bar with different categories of services, which is where you can begin your journey.

## Understanding the AWS Free Tier
AWS offers a Free Tier for new customers to explore its platform. The Free Tier is designed for individuals who want to learn about AWS without incurring costs. It provides a selection of services that are free to use up to a specific usage limit each month. This is a great opportunity to get hands-on experience with cloud technology.

### What’s Included in the Free Tier?
The AWS Free Tier has three main types of offerings:

- **Always Free**: These services are always free within certain limits, regardless of when you start using them. Examples include Amazon S3 (storage), AWS Lambda (compute), and Amazon DynamoDB (database). Each service has its own usage limits, and exceeding these limits may result in charges.
- **12-Month Free**: These services are free for the first 12 months after you sign up for AWS. After the first year, you will begin incurring charges. Examples include Amazon EC2 (virtual servers) and Amazon RDS (relational database services). You can experiment with these services, keeping track of your usage to avoid charges.
- **Trials**: Some AWS services offer short-term free trials, which give you access to premium features for a limited time. These trials typically last for one month and provide access to a set amount of resources.

### Free Tier Limits and Usage
AWS Free Tier limits vary by service, and each service has a set of rules about what constitutes "free" usage. It’s important to monitor your usage to ensure that you don’t accidentally exceed these limits. For instance:
- **Amazon EC2 (virtual servers)**: You get 750 hours per month of free usage, which is enough to run one small instance continuously for the entire month.
- **Amazon S3 (storage)**: You get 5GB of standard storage, along with 20,000 GET and 2,000 PUT requests.
- **AWS Lambda (serverless computing)**: You get 1 million free requests per month, which allows you to experiment with serverless applications.

AWS provides tools to help you monitor your Free Tier usage, such as the AWS Billing and Cost Management dashboard, which you can use to track your spending and usage patterns.

## How to Learn and Experiment with AWS Using the Free Tier

### Focus on One Service at a Time
As AWS offers a broad range of services, it’s best to focus on learning one service at a time to avoid feeling overwhelmed. Instead of trying to learn everything at once, you can start with fundamental services that help you understand the core concepts of cloud computing.

For example, you can start by experimenting with Amazon EC2 to launch a virtual machine (also known as an instance) and learn the basics of virtual servers. Similarly, you can try out Amazon S3 to learn about cloud storage, or explore AWS Lambda to get a feel for serverless computing. The AWS Free Tier allows you to try these services without worrying about costs, as long as you stay within the usage limits.

### Follow AWS Training Resources
AWS offers a wealth of training and educational resources to help beginners get started. Here are some key resources you can use:
- **AWS Training and Certification**: AWS provides free digital training courses for beginners, covering a variety of cloud topics. These courses include videos, tutorials, and self-paced learning options. You can also opt for certifications that can validate your skills and knowledge in AWS.
- **AWS Documentation**: AWS has comprehensive documentation for all its services. It provides step-by-step tutorials, code examples, and explanations to help you learn and troubleshoot any challenges.
- **AWS Educate**: This is an initiative by AWS that offers students, educators, and educational institutions free resources to learn about cloud computing. It includes hands-on labs, courses, and access to AWS credits.
- **AWS Whitepapers**: For those interested in diving deeper into AWS’s infrastructure, AWS publishes detailed whitepapers that explain the architectural best practices and design patterns for building systems on AWS.

### Utilize AWS Tutorials and Labs
AWS provides hands-on tutorials to walk you through various tasks using the Free Tier. These tutorials are interactive and help you learn by doing. AWS also offers “AWS Labs,” which are open-source projects with instructions on how to create specific applications using AWS services. They are a great way to experiment with new services and build real-world applications.

### Join the AWS Community
Joining the AWS community is a great way to stay up-to-date with the latest trends, learn from others, and ask questions. AWS has forums, Slack channels, and online groups where people from all over the world come together to discuss solutions, share experiences, and help each other.
- **AWS re:Invent**: This is an annual event where AWS customers and developers come together for sessions and workshops. It’s an excellent place to learn new skills and hear from AWS experts.
- **AWS Meetups**: AWS regularly hosts meetups around the world for people interested in cloud computing and AWS. These meetups offer a chance to network, ask questions, and learn in a collaborative environment.

### Monitor Your Usage
One of the most important aspects of using AWS is managing your usage to ensure that you don’t incur unexpected costs. AWS provides tools such as the AWS Cost Explorer and AWS Budgets to track and manage your spending. These tools will send alerts when you're getting close to your Free Tier limits, so you can avoid accidental charges.

## Transitioning to Paid Services
Once you’re comfortable with AWS and have learned about the various services, you might start using resources that go beyond the Free Tier limits. This could involve:
- Running more powerful EC2 instances,
- Storing larger amounts of data in S3, or
- Scaling up your application.

At that point, you may want to explore AWS’s pricing options and cost management strategies to control expenses.

### Understanding Pricing Models
AWS pricing can be complex, as it is based on a pay-as-you-go model. You pay for what you use, and prices vary depending on the service and region. AWS offers pricing calculators that can help you estimate your costs based on your expected usage.

### Cost Optimization
AWS provides a suite of tools to help you optimize costs. You can use AWS Trusted Advisor to identify underutilized resources and receive recommendations on cost-saving opportunities. Additionally, AWS offers a Savings Plans program, where you commit to using specific services for a longer period at a discounted rate.


## Step 2: What is AWS CLI, and Why Do We Need It?

**AWS CLI** stands for **Amazon Web Services Command Line Interface**. It is a powerful tool that allows you to manage and interact with AWS services directly from your computer’s command line or terminal.

Think of it as a way to control AWS resources, like EC2 instances, S3 buckets, and more, all through text commands, instead of having to click through the AWS Management Console on the web. This can save you a lot of time, especially when automating tasks or managing multiple AWS services.

With AWS CLI, you can:

- Launch and manage AWS resources.
- Automate processes like backups, updates, and deployments.
- Manage permissions and security settings.
- View logs, monitor usage, and control other aspects of your AWS environment, all from your terminal.

### Why Do You Need AWS CLI?

AWS offers a lot of services, but manually clicking through the console to configure or manage each service can be slow and inefficient. With AWS CLI, you can automate tasks, use scripts to interact with services, and even manage multiple AWS accounts.

The main reasons you might want to use AWS CLI are:

- **Speed**: Execute tasks faster than manually using the console.
- **Automation**: Automate tasks using scripts.
- **Efficiency**: Control multiple AWS resources and services with a single command.
- **Advanced Use**: Some AWS features and configurations are only accessible via the CLI.

### How to Download and Install AWS CLI?

Before you start using AWS CLI, you need to install it on your machine. Here’s how to do it:

#### 1. Download AWS CLI

AWS CLI is supported on multiple operating systems such as Windows, macOS, and Linux. Below are the installation steps for each:

#### For Windows:

1. Download the latest AWS CLI MSI installer from this link: [AWS CLI MSI installer](https://aws.amazon.com/cli/)
2. Run the installer and follow the on-screen instructions.
3. Once installed, you can verify it by typing `aws --version` in the Command Prompt.

#### For MacOS:

1. Open the Terminal.

2. Use the Homebrew package manager to install AWS CLI by running:

    ```bash
    brew install awscli
    ```

3. If you don’t have Homebrew installed, you can download AWS CLI from the official website.

4. To verify the installation, run:

    ```bash
    aws --version
    ```

#### For Linux:

1. Open a terminal window.
2. Download and install AWS CLI using the package manager:

   ### For Ubuntu/Debian:
   ```bash
   sudo apt-get update
   sudo apt-get install awscli
   ```

   ### For CentOS/RedHat
   ```bash
   sudo yum install awscli
   ```

3. Verify the installation by running
   ```bash
   aws --version
   ```

#### 2. Check Installation

Once installed, you can verify that AWS CLI is working by typing the following command in your terminal or command prompt:

```bash
aws --version
```
### How to Configure AWS CLI

After installing AWS CLI, the next step is to configure it with your AWS credentials. AWS CLI requires access keys (your AWS Access Key ID and Secret Access Key) in order to interact with your AWS account.

#### 1. Generate AWS Access Keys:
- Sign in to the AWS Management Console.
- Go to the **IAM (Identity and Access Management)** section.
- In the left sidebar, click on **Users**, then select the user you want to create keys for (usually yourself).
- Under the **Security credentials** tab, you will see **Access keys**. Click on **Create New Access Key** and download the keys.

#### 2. Configure AWS CLI:
Once you have the Access Key ID and Secret Access Key, open your terminal or command prompt and run the following command:

```bash
aws configure
```

This command will prompt you to enter the following details:

- **AWS Access Key ID**: (Enter the Access Key you got from the AWS console)
- **AWS Secret Access Key**: (Enter the Secret Access Key you got from the AWS console)
- **Default region name**: (Enter the AWS region, such as us-east-1)
- **Default output format**: (Choose a format like json, text, or table)

```bash
$ aws configure
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: us-east-1
Default output format [None]: json
```
#### 3. Once you’ve entered this information, the AWS CLI will store it in your system, and you can start using the commands to manage your AWS services.

**Verifying a Successful Installation**

After configuring AWS CLI, you can verify that everything is set up correctly by running a simple AWS CLI command to list your S3 buckets (if you have any):

```bash
aws s3 ls
```

### AWS CLI Setup and Troubleshooting

If everything is set up correctly, it will return a list of your S3 buckets. If you don’t have any, it will just return an empty list. If there’s an error with your configuration, you will see an error message, and you can troubleshoot the issue.

#### 1. Command Not Found:
If you see an error like `command not found: aws`, make sure AWS CLI is correctly installed. You may need to add the installation path to your system’s environment variables.

#### 2. Access Denied:
If you get an "Access Denied" error, double-check that your Access Key ID and Secret Access Key are correct and have sufficient permissions to perform the operation you’re trying to do.

#### 3. Incorrect Region:
If you see errors related to the region, ensure you’ve configured the correct region with `aws configure`.

## Step 3: Understanding AWS Credentials and Config Files

When you work with Amazon Web Services (AWS), there are two key files that play a critical role in authenticating and configuring your AWS access: ~/.aws/credentials and ~/.aws/config. These files are essential for interacting with AWS services in a secure and structured manner, whether you are using the AWS Command Line Interface (CLI), SDKs, or any other tools that require access to AWS resources.

### What are the credentials and config Files?

In AWS, you typically access your resources using credentials (like an access key) and configuration settings (like region). These files are where you store the necessary information to authenticate yourself and define how you want to interact with AWS.

- **~/.aws/credentials**: This file contains your access keys. It stores the access key ID and secret access key that are used to authenticate your AWS API requests.

- **~/.aws/config**: This file contains configuration settings for AWS tools, including default regions and output formats.

Both files are typically stored in a hidden directory in your home folder (~/.aws/).

#### Location of these files:

- **Linux/Mac**: ~/.aws/credentials and ~/.aws/config

- **Windows**: C:\Users\YourUsername\.aws\credentials and C:\Users\YourUsername\.aws\config

### Why do we need these files:
When interacting with AWS, especially through the AWS CLI or SDKs, your application or command-line tools need a way to authenticate with AWS. AWS uses access keys and secret keys to verify that requests to AWS are coming from a trusted source (you or your application).

Rather than hardcoding these keys into your application (which would be risky and insecure), AWS encourages you to store this information securely in the ~/.aws/credentials file. This allows you to manage your keys securely and use them across multiple tools without exposing sensitive information.

Similarly, the ~/.aws/config file contains settings like your default region (e.g., us-east-1) and preferred output format (e.g., json or text). These configurations help streamline your workflow and ensure your requests are directed to the right region.

### How do the credentials and config files work?
Let’s break down the workflow of how these files interact with AWS tools and why they are structured the way they are:

#### 1. Storing AWS Credentials
In the credentials file, you store the AWS access key ID and secret access key. These credentials are tied to an AWS IAM user or role that has permissions to access certain AWS resources.
```bash
   [default]
   aws_access_key_id = YOUR_ACCESS_KEY_ID
   aws_secret_access_key = YOUR_SECRET_ACCESS_KEY

   [profile1]
   aws_access_key_id = ACCESS_KEY_1
   aws_secret_access_key = SECRET_KEY_1
```

In this example:
- The **[default]** profile is the default set of credentials you use for AWS operations.
- The **[profile1]** profile is an alternative set of credentials you can use for other operations.

The credentials are used by AWS tools to authenticate your requests. If you're using the AWS CLI, for example, it looks for credentials in the credentials file to authenticate your request.

#### 2. Setting Up AWS Configuration
The config file stores configuration settings such as the default region (where AWS resources are created) and the output format (how the results of commands should be displayed).
```bash
   [default]
   region = us-east-1
   output = json

   [profile1]
   region = us-west-2
   output = text
```

In this example:
- The **[default]** section sets the default AWS region (e.g., us-east-1) and the output format (e.g., json).
- The **[profile1]** section specifies a different region (us-west-2) and output format (text).

This configuration helps AWS tools know where to direct your requests (in terms of region) and how you want the results to be formatted.

#### 3. AWS CLI uses these files

When you run a command in the AWS CLI, it first looks for the ~/.aws/config and ~/.aws/credentials files to determine how to authenticate and which region to send requests to.

- If you run a command without specifying a profile, the AWS CLI uses the default profile by looking in both the config and credentials files.

- If you specify a profile using the --profile flag, the CLI uses the corresponding profile from both files.

```bash
   aws s3 ls --profile profile1
```

This will list all S3 buckets, using the credentials and region configuration defined in the profile1 section.

#### 4. Complete workflow of these files:

Here’s a simplified workflow of how AWS tools use the credentials and config files:

1. **Set up IAM user and permissions**: In the AWS Console, create an IAM user and assign them the necessary permissions (like access to S3, EC2, etc.). You will receive an access key ID and secret access key for this user.

2. **Configure your environment**: Using the AWS CLI or SDK, configure your environment to store these credentials:
   - Run aws configure to set up the default profile, where you’ll input the access key ID, secret access key, default region, and output format.
   - Alternatively, you can manually edit the ~/.aws/credentials and ~/.aws/config files.

3. **Use the AWS tools**: Now, whenever you run AWS CLI commands or interact with AWS SDKs, the tools will check the ~/.aws/credentials and ~/.aws/config files to authenticate your requests and use the correct region and output format.

4. **Access AWS Resources**: When you execute a command, the AWS tools use the stored credentials to authenticate your identity and then send the request to the appropriate region as defined in the config file.

5. **Secure Your Credentials**: It's essential to never expose your access key or secret access key in your code, in public repositories, or in shared spaces. The credentials file is a safer alternative.

## Step 4: How to verify AWS configuration details on your machine

When you start working with Amazon Web Services (AWS), it’s essential to properly configure your system to interact with AWS resources. This configuration often involves setting up your AWS access keys, choosing the AWS region, and specifying other settings that define how you interact with the AWS Cloud.

If you’ve already configured AWS on your machine using the AWS Command Line Interface (CLI) or AWS SDKs, you might need to verify that your configuration is set up correctly. It’s important to check your configuration to ensure that your credentials, region, and other settings are correct — especially before you run commands that interact with your AWS resources.

### How to Check What AWS Configuration is Set Up on Your Machine

There are several ways to verify and check the AWS configuration details on your machine. Let’s go through them step by step.

#### Step 1: Check the AWS Configuration Files
The first place to check is the configuration files themselves. These files are where AWS stores the settings you’ve configured.

1. Open your terminal (or command prompt on Windows).

2. Navigate to the .aws directory. This is where your credentials and config files are stored:

- Linux/macOS: ```cd ~/.aws```
- Windows: ```cd C:\Users\YourUsername\.aws```

3. Open the credentials and config files in any text editor. You’ll find the AWS configuration details stored here.

    ```/.aws/credentials```
    ```bash
   [default]
   aws_access_key_id = YOUR_ACCESS_KEY_ID
   aws_secret_access_key = YOUR_SECRET_ACCESS_KEY

   [profile1]
   aws_access_key_id = ACCESS_KEY_1
   aws_secret_access_key = SECRET_KEY_1
    ```
    ```~/.aws/config```
    ```bash
   [default]
   region = us-east-1
   output = json

   [profile1]
   region = us-west-2
   output = text
    ```
    The credentials file stores the AWS access keys for different profiles.

    The config file stores configuration settings like the region and output format for each profile.

#### Step 2: Use the AWS CLI to Verify Configuration

If you don’t want to manually open the files, you can use the AWS CLI to check your configuration. AWS provides several commands that allow you to check and verify your settings.

1. To verify if the AWS CLI is properly configured, you can use the aws configure list command. This command shows you all the configuration details AWS CLI is using.

    ```aws configure list```
    ```bash
       Name                    Value                    Type           Location
       ----                    -----                    -----          --------
     access_key         ****************ABCDEF       config_file    ~/.aws/credentials
     secret_key         ****************XYZ123       config_file    ~/.aws/credentials
     region                  us-east-1               config_file    ~/.aws/config
     output                    json                  config_file    ~/.aws/config
    ```
2. Another way to verify that your configuration is correct is by running a simple AWS CLI command that requires authentication, such as aws sts get-caller-identity.

    This command fetches the identity of the AWS user making the request and confirms that your credentials are working correctly.

    ```aws sts get-caller-identity```

    ```
    {
    "UserId": "AROAEXAMPLEID",
    "Account": "123456789012",
    "Arn": "arn:aws:iam::123456789012:user/YourUser"
    }
    ```

## Step 5: How to Configure Multiple AWS Profiles on Your Machine.

Amazon Web Services (AWS) allows you to manage and interact with a wide variety of cloud services such as storage, compute power, databases, and networking. Often, when working with AWS, you might need to interact with more than one AWS account, environment, or project. This is where the concept of AWS profiles becomes essential.

### Why do you need multiple AWS Profiles.
In real-world scenarios, there are many reasons you might want to use multiple profiles. Some of the common use cases include:

1. **Managing Multiple AWS Accounts**: You might have separate AWS accounts for different projects, environments (e.g., development, testing, production), or teams. With multiple profiles, you can easily switch between them.
2. **Role-based Access**: You may be working with an AWS account that has different IAM roles (e.g., admin, read-only, developer). Each role can have its own set of permissions and credentials, which you can configure using separate profiles.
3. **Work and Personal Accounts**: If you’re working with AWS for both personal projects and work-related projects, you might want to have separate profiles to keep everything organized and secure.

### How do you configure multiple AWS Profiles on your machine

AWS CLI allows you to configure and use multiple profiles on your machine. Each profile stores its own credentials and configuration settings in the configuration files.

1. **Configure the Default Profile**: Before adding multiple profiles, it’s a good idea to set up the default profile first. This profile will be used if you don’t specify a profile in your commands.
   - Open your terminal (or command prompt on Windows).
   - Run the following command to start configuring your AWS credentials:

        ```aws configure```
   - AWS CLI will prompt you for the following details:

        **AWS Access Key ID**: You get this from the IAM user you created in the AWS console.

        **AWS Secret Access Key**: The secret key corresponding to the access key.

        **Default region name**: This is the AWS region where you want to interact with services by default (e.g., us-east-1).

        **Default output format**: The format in which you want AWS CLI to display results (e.g., json, text, or table).

        ```bash
        $ aws configure
        AWS Access Key ID [None]: YOUR_ACCESS_KEY_ID
        AWS Secret Access Key [None]: YOUR_SECRET_ACCESS_KEY
        Default region name [None]: us-east-1
        Default output format [None]: json
        ```
       This will set up your default profile and store these details in the ~/.aws/credentials and ~/.aws/config files.

2. **Add Additional Profiles**: To configure additional profiles, you’ll need to specify the --profile flag when running the aws configure command. This allows you to create multiple profiles, each with its own credentials and configuration settings.

    ```aws configure --profile profile1```

    AWS CLI will prompt you for the following details again, but this time the settings will be saved under the [profile profile1] section in the ~/.aws/credentials and ~/.aws/config files.

    Repeat this process for any other profiles you want to create. You can name the profiles whatever you like (e.g., dev, prod, admin, etc.).

3. The **~/.aws/credentials and ~/.aws/config file** will look like this:
    ```bash
   [default]
   aws_access_key_id = YOUR_DEFAULT_ACCESS_KEY_ID
   aws_secret_access_key = YOUR_DEFAULT_SECRET_ACCESS_KEY

   [profile1]
   aws_access_key_id = YOUR_PROFILE1_ACCESS_KEY_ID
   aws_secret_access_key = YOUR_PROFILE1_SECRET_ACCESS_KEY
    ```
    ```bash
    [default]
   region = us-east-1
   output = json

   [profile profile1]
   region = us-west-2
   output = text
   ```

4. Using Different profiles with AWS CLI: Once you have multiple profiles set up, you can use them in your AWS CLI commands by specifying the --profile flag.

    For example, to list S3 buckets using the profile1 profile, run:

    ```aws s3 ls --profile profile1```

    If you don’t specify a profile, the AWS CLI will use the default profile.

## Step 6: How to set AWS Credentials as Environment Variables without using configuration Files

When working with Amazon Web Services (AWS), it's common to authenticate your machine using access keys (access key ID and secret access key) and specify a region for your resources. One way to configure AWS is by using configuration files like ~/.aws/credentials and ~/.aws/config. However, there are situations where you might not want to store sensitive information like your AWS credentials directly in these files.

Instead, you can configure AWS by setting environment variables for your credentials. This approach can be more secure because it avoids storing sensitive information in plain text files. It also gives you more flexibility, especially if you want to switch between different AWS profiles quickly or work in temporary environments.

### Why You Might Not Want to Store Credentials in Configuration Files
While storing AWS credentials in configuration files is a common approach, there are certain scenarios where you might want to avoid it:

1. **Security Concerns**: Storing sensitive information like AWS credentials in plain text files can be risky, especially if someone else gains access to your machine. This is especially true in shared or public environments.

2. **Temporary or Dynamic Environments**: If you’re working in temporary or automated environments (e.g., CI/CD pipelines, development containers, or on an EC2 instance), you may not want to store credentials persistently. Instead, you can use environment variables to pass the credentials dynamically for the duration of the session.

3. **Easier Credential Rotation**: Storing credentials as environment variables allows you to easily change them for different sessions or switch between multiple profiles without modifying files directly.

### Setting AWS Credentials as Environment Variables
The AWS CLI and SDKs allow you to set the necessary values (access key ID, secret access key, region, and output format) using environment variables. This way, you don't need to store these details in the configuration files. Let’s go through how to set each of these values.

1. **Linux/Mac**:
   - Open your terminal.
   - Use the export command to set the variables for the current session.
     ```bash
     export AWS_ACCESS_KEY_ID=YOUR_ACCESS_KEY_ID
     export AWS_SECRET_ACCESS_KEY=YOUR_SECRET_ACCESS_KEY
     export AWS_DEFAULT_REGION=us-east-1
     export AWS_DEFAULT_OUTPUT=json
     ```
2. **Windows**
   - Open the Command Prompt.
   - Use the set command to set the environment variables.
     ```bash
     set AWS_ACCESS_KEY_ID=YOUR_ACCESS_KEY_ID
     set AWS_SECRET_ACCESS_KEY=YOUR_SECRET_ACCESS_KEY
     set AWS_DEFAULT_REGION=us-east-1
     set AWS_DEFAULT_OUTPUT=json
     ```

### Which method should you prefer: Environment Variables or Configuration Files?

- **Using Environment Variables**

    **Pros**:

    ***Security***: Credentials are not stored in files on your system, reducing the risk of accidental exposure (e.g., through file sharing).

    ***Flexibility***: Environment variables allow you to change credentials dynamically for each session, making it ideal for temporary environments (like CI/CD pipelines or development containers).

    ***No File Permissions***: You don't need to worry about file access permissions for the ~/.aws/credentials or ~/.aws/config files.

    **Cons**:

    ***Temporary***: Environment variables are only active for the current session. If you close your terminal or log out, you’ll need to reset them.

    ***Manual Setup***: You have to manually set environment variables each time you want to use AWS credentials, unless you automate this process (e.g., by adding them to your .bashrc or .zshrc file on Linux/Mac).

- **Using Configuration Files**

    **Pros**:

    ***Persistence***: Credentials and configurations are saved to files, so you don’t need to manually set environment variables every time you work with AWS.

    ***Multiple Profiles***: It’s easier to manage multiple profiles (e.g., for different AWS accounts or environments) using configuration files.

    ***Built-in Support***: AWS CLI and SDKs natively support configuration files, so you don’t have to worry about setting up environment variables.
    
    **Cons**:

    ***Security Risk***: Storing credentials in plain text files can be a security risk, especially if the files are not properly protected or if you share your system with others.

    ***Less Flexibility***: If you want to switch credentials or regions quickly, it can be more cumbersome than using environment variables.
    








