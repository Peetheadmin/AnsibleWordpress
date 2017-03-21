# CFT to automate installatin of Wordpress using Ansible

Setup Wordpress on ubuntu linux EC2 instance using ansible and automate this using a cloud formation template

**Objective**:

Use CM tools such as Puppet, Ansible, or Chef to automate the installation of basic Drupal or WordPress.Setup a sample site. Automate the solution using Cloudformation template.

**Deliverable**:

A cloudformation template that accepts user inputs as parameters where applicable ( for example, Admin password). This template should setup VPC, create subnets, launch a CM instance, pull the necessary code (modules, classes, recipes etc) from a GIT repo (or S3), and configure the web instance for basic Drupal or Wordpress setup.

**Approach**:

Step 1: For this assessment, I set up a test environment on VMWare Workstation to install wordpress on localhost using ansible(I'm a Ubuntu Linux image).

Step 2: Created a playbook for the installation of Apache, MySQL, PHP, Wordpress in the test Environment.

Step 3: After success of Step 2, I pushed this playbook to my GitHub account.

Step 4: Built a CloudFormation Template with resources mentoined in the Deliverable,This CFT takes user input like username, password,etc; and sets this parameters to the EC2 instance.

Step 5: In the cloud Formation Template, the Userdata section I installed necessary packages(aws-cli, cfn-heat ...) and downloaded the repository mentioned in Step3 from my GitHub account.

Step 6: Tested the functioning of the CFT and published the Repository on GitHub.

**To Build the stack**:

1. Download  this repository https://github.com/sriramgaddipati/UbuntuAnsible .

2. Create a stack using CloudFormation.json file in cloud formation.

3. Fill parameters of Stackname, DatabaseName, DBUser, DBPassword.. and choose an existing keypair for SSH connection.

4. The User parameters will give you access to corresponding mysqlDB and user on EC2 instance built.

**Output**:

Stack up and running, able to access EC2 instance and MySQLDB with input username and password. 


<img width="1280" alt="built stack" src="https://cloud.githubusercontent.com/assets/19828746/24136041/539ca676-0de3-11e7-9d24-b1d8a0611740.png">

