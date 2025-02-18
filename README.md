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
1. We first go to the AWS EC2 Console:
   - We open our AWS Management Console and navigate to EC2 or search for it.
2. We launch a New Instance:
   - We click on Launch Instance.
3. We choose an Amazon Machine Image (AMI):
   - An Amazon Machine Image (AMI) is a pre-configured template that contains the necessary software, operating system, and application environment required to launch an EC2 instance in AWS. AMIs help us quickly deploy instances with consistent configurations, reducing setup time and ensuring scalability.
   - We select the Amazon Linux AMI.
4. We choose the Instance Type:
   - We select t2.micro (suitable for basic web applications).
5. We select the Key Pair:
   - We create a new key pair named ** task_2 **for SSH access.
6. We configure Network Settings:
   - We enable Public IP (for internet access).
   - We allow HTTP (port 80) for web application access.
7. We launch the Instance:
   - Finally, we click Launch Instance and wait for it to start.

**Step 2: Set Up CloudWatch Alarms**
1. We go to the AWS CloudWatch Console:
   - We open CloudWatch from the AWS console.
2. Create an Alarm:
   - We click on Alarms > Create Alarm:
3. Choose a Metric:
   - We click Select metric > EC2 > Per-instance Metrics:
   - We select CPUUtilization (or another metric like Network In/Out).
4. Set the Condition:
   - If CPU Utilization > 80% for 2 consecutive periods.
5. Set Actions:
   - We choose EC2 Actions > Stop this instance (to stop the instance when the threshold is reached).
6. Review and create.
   - We click Next, review the alarm, and Create Alarm.

**Step 3: Monitor Application Using CloudWatch Metrics**
1. We go to the EC2 Console:
   - We open the EC2 Dashboard.
2. We access CloudWatch Metrics:
   - We navigate to Monitoring > View all CloudWatch metrics.
3. We select Metrics to Monitor:
   - We click EC2 > Per-instance Metrics.
   - We choose metrics like:
     - EBS Write Operations
     - Network In/Out
     - CPU Utilization
4. We view Metrics Graphs:
   - We will see real-time graphs for the selected metrics.

**Step 4: Create a CloudWatch Dashboard:**
1. We go to the CloudWatch Dashboard:
   - We open CloudWatch from the AWS Console.
   - We create a New Dashboard.
2. We click Dashboards > Create dashboard:
   - We enter a dashboard name.
   - We add Widgets.
3. We choose a Widget Type (Graph, Number, Table):
   - We select CloudWatch as the Data Source.
   - We select Metrics to Monitor.
4. We click Save to finalize our monitoring dashboard.
