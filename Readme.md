
## CloudTrail - Create a Trail
AWS CloudTrail is a service that captures every event occurred in your account, in the form of logs, for review and analysis. These logs can be stored in Amazon S3 buckets or delivered to Amazon CloudWatch logs, which helps you to set alarms and take appropriate actions.  


### A. CloudTrail Dashboard  
Navigate to the CloudTrail dashboard, and launch the wizard to create a trail.  

![trail](trail.png?raw=true "trail")

### B. Create a Trail  
AWS provides a quick trail create process, where you just have to specify the display name for your trail, and an S3 bucket to store logs.  

1. Quick process  
The Quick trail create wizard will automatically create an S3 bucket and folder on your behalf to store the logs. The folder in the newly created S3 bucket is aws-cloudtrail-logs-572815612669-96486641, and the folder is AWSLogs/572815612669/CloudTrail/. It will create further sub-folders based on your region name, year, month, and date.  

![trail2](trail2.png?raw=true "trail2")

2. Regular process
If you wish to use an existing S3 bucket, you will have to navigate to the detailed Create trail process. You can launch one from the CloudTrail dashboard. The regular Create trail is a three-step process:  
Step 1 - General details - Provide the trail name, choose the new/existing S3 bucket, and enable/disable the encryption.  

If the encryption is enabled, CloudTrail will encrypt log files by using the AWS Key Management Service (SSE-KMS). In addition, you can choose to be notified each time a log is delivered to your bucket. There is another feature, log digest, to verify that your log files did not change after CloudTrail delivered them.  


Step 2 - Events and Management details - Choose the types of events you want to log. There are three categories of events - Management events, Data events (operations performed within a resource), and Insights events (unusual activity, errors, or user behavior).  
![trail3](trail3.png?raw=true "trail3")

![trial4](trail4.png?raw=true "trial4")
![trail5](trail5.png?raw=true "trail5")

### C. Dashboard
The CloudTrail dashboard displays an overview of all your trails, insights, and event history. 

Consider a Trail as a log of all the events/actions that occurred in your AWS account. Of course, events have to be processed to convert them into a particular log-format.  

![trail6](trail6.png?raw=true "trail6")

In the snapshot above, notice the separate table for Trails, Insights, and Event history. The Event history section shows all the recent events. It shows every action that occurred in your AWS account. Click on View full Event history to see additional details and more events that have occurred.  

Remember, that the first trail does not attract billing charges. However, you incur charges for the S3 bucket that will store your logs. You can create additional trails on a charge-basis.  

