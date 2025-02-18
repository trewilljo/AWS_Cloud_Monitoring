# AWS_Cloud_Monitoring


*COMPANY*: CODTECH IT SOLUTIONS 

*NAME*: Aastha Joshi

*INTERN ID*: CT08OHH

*DOMAIN*: CLOUD COMPUTING

*BATCH DURATION*: JANUARY 20,2025 to FEBRUARY 20,2025

*MENTOR NAME*: NEELA SANTOSH

# Description

### **Amazon EC2 (Elastic Compute Cloud):** ###
Is a cloud-based virtual server that provides scalable and on-demand computing power, helping businesses reduce hardware costs and deploy applications faster. It allows users to launch, configure, and manage virtual servers called EC2 instances, with various instance types offering different hardware configurations. EC2 enables easy scaling, allowing users to increase capacity to handle traffic spikes or reduce capacity when demand decreases.

### **Amazon CloudWatch:** ###
Is a real-time monitoring service that collects and tracks metrics from AWS resources and applications. It provides insights into system performance, automatically displaying metrics for AWS services and allowing users to create custom dashboards for monitoring specific applications. CloudWatch also enables users to set up alarms that trigger notifications or automated actions when predefined thresholds are met.

### **Amazon CloudWatch Dashboards:** ###
Offer a centralized, customizable view of AWS resources across multiple regions. They allow users to monitor key metrics, visualize trends, and create operational playbooks for efficient incident response. By customizing dashboards with selected metrics, alarms, and color-coded graphs, teams can enhance visibility and streamline communication during critical events. Together, EC2 and CloudWatch provide a robust solution for managing, monitoring, and optimizing cloud-based applications.

# Task:
- SET UP MONITORING FOR A CLOUDBASED APPLICATION USING AWS CLOUDWATCH.

# Procedure:

**Step 1: Create an EC2 Instance:**
1. We first go to AWS EC2 Console:
   - As we Open our AWS Management Console and go to EC2 or search it.
2. We  launch a New Instance:
   - Click Launch Instance.
3. Choose an Amazon Machine Image (AMI):An Amazon Machine Image (AMI) is a pre-configured template that contains the necessary software, operating system, and application environment required to launch an EC2 instance in AWS. AMIs help users quickly deploy instances with consistent configurations, reducing setup time and ensuring scalability.
   - Select Amazon Linux AMI.
4. Choose Instance Type:
   - Select t2.micro (for basic web applications).
5. Select Key Pair:
   - We create a new key pair name task_2 for SSH access.
6. Configure Network Settings:
   - We enable Public IP (for internet access).
   - We allow HTTP (port 80) for web application access.
7. Launch the Instance:
   - Laastly, we click Launch Instance and wait for it to start.

**Step 2: Set Up CloudWatch Alarms**
1. Go to AWS CloudWatch Console
   - Open CloudWatch from the AWS console.
   - Create an Alarm

2. Click on Alarms > Create Alarm.
   - Choose a Metric

3. Click Select metric > EC2 > Per-instance Metrics.
   - Select CPUUtilization (or another metric like Network In/Out).
   - Set Condition

Example: If CPU Utilization > 80% for 2 consecutive periods.
Set Actions

4. Choose EC2 Actions > Stop this instance (to stop the instance when the threshold is reached).
   - Review and Create

5. Click Next, review the alarm, and Create Alarm.
