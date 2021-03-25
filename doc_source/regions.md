# AWS Regions and IP Address Ranges<a name="regions"></a>

AWS cloud computing resources are housed in highly available data center facilities in different areas of the world \(for example, North America, Europe, or Asia\)\. Each data center is part of an AWS Region\. Each AWS Region contains two or more data centers, which are called Availability Zones \(AZs\)\. For more information about AWS Regions and AZs, see [Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)\.

Amazon QuickSight is currently supported in the following AWS Regions and IP address ranges\. 


| AWS Region | IP Address Range | 
| --- | --- | 
| US East \(Ohio\) \(us\-east\-2\) | 52\.15\.247\.160/27 | 
| US East \(N\. Virginia\) \(us\-east\-1\) | 52\.23\.63\.224/27 | 
| US West \(Oregon\) \(us\-west\-2\) | 54\.70\.204\.128/27  | 
| EU \(Frankfurt\) \(eu\-west\-1\) | 35\.158\.127\.192/27 | 
| EU \(Ireland\) \(eu\-west\-1\) | 52\.210\.255\.224/27 | 
| EU \(London\) \(eu\-west\-2\) | 35\.177\.218\.0/27 | 
| Asia Pacific \(Mumbai\) | 52\.66\.193\.64/27 | 
| Asia Pacific \(Seoul\) | 13\.124\.145\.32/27 | 
| Asia Pacific \(Singapore\) | 13\.229\.254\.0/27 | 
| Asia Pacific \(Sydney\) | 54\.153\.249\.96/27 | 
| Asia Pacific \(Tokyo\) | 13\.113\.244\.32/27 | 
| Canada \(Central\) | 15\.223\.73\.0/27 | 
| South America \(São Paulo\) | 18\.230\.46\.192/27 | 

When you sign up for Amazon QuickSight, you select a home AWS Region\. This is the AWS Region where you want Amazon QuickSight to allocate the initial SPICE capacity associated with any user accounts you create\. Typically, this will be the AWS Region closest to your physical location, and the same AWS Region where you have the majority of your other AWS resources \(like Amazon RDS instances\)\. For more information about how SPICE capacity is allocated, see [Managing SPICE Capacity](managing-spice-capacity.md)\.

When you sign in to Amazon QuickSight using the default URL of aws\.amazon\.com/quicksight, the US East \(N\. Virginia\) \(us\-east\-1\) region is selected by default\. If you sign in using a URL that specifies a supported AWS Region, for example us\-west\-2\.quicksight\.aws\.amazon\.com, the AWS Region specified in the URL is selected\. You can change to other supported AWS Regions by using the region selector on the right side of the application bar\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/region-selector.png)

You can autodiscover your Amazon RDS instances and Amazon Redshift clusters that run in any of the AWS Regions that Amazon QuickSight supports\. If you enable autodiscovery, the autodiscovered resources displayed reflect whatever AWS Region you currently have selected\. You can still use AWS resources in other AWS Regions by manually creating connections to them\. For more information about enabling autodiscovery of AWS data stores, see [Authorizing Connections from Amazon QuickSight to AWS Data Stores](enabling-access.md)\. 

It is important to remember that each AWS Region is completely independent\. Any Amazon QuickSight resources you create, like data sets and analyses, exist only in the AWS Region in which you create them, and can't be moved to other AWS Regions\. 
