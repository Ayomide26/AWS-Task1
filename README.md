### Create a static website and host it on S3 bucket(private bucket) but with public read policy assigned, using cloud front for CDN.

## Step 1 - Creating a Bucket on Amazon S3
###  After logging into your AWS Console, under Services > All Services, search for “S3” and click on it to go to the S3 dashboard.
![installation](https://github.com/Ayomide26/Aws-Task1/blob/main/images/firsts3.PNG)
### On the S3 Dashboard, click on the Create Bucket button to create a new storage bucket to store your static website files.
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/stepp1.PNG)

## Step 2 - Upload Website files to S3 Bucket
### After creating a new bucket, click on the bucket name to view the bucket details.

### On the File Upload page, click on the Add files to add a file from your computer, or Add folder to add multiple files from a folder.

### Once the uploading process has completed, you may check if each file has been uploaded successfully or if there are any errors. Otherwise, just click on the Close button to return to the Bucket details screen.
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/stepp2.PNG)

## Step 3 - Enabling Static Website Hosting on S3 Bucket
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/step3.PNG)

## Step 4 - Creating a CloudFront Distribution
### From the top navigation under Services > All Services, search for “CloudFront” and click on it.
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/cloudfront.PNG)
### On the CloudFront Distributions page, click on the Create distribution button.
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/createdi.PNG)
### On the Create distribution page > under Origin section > for Origin domain > enter the Amazon S3 static website endpoint 
### Leave other settings under Default cache behavior section to the default
### Enter “index.html” for Default root object. This file name must match with the index document file name
### Leave other settings intact. Scroll to the bottom and click on the Create distribution button.
### As you remember from earlier, CloudFront will now distribute all your files to edge locations around the world. This process will take some time to complete.
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/step6.PNG)
## Step 5 - Add a Bucket Policy
###  On the Bucket overview page, click on the Permissions tab, scroll down and look for Bucket policy section.
### On the Bucket policy section, click on the Edit button. To grant public read access for your website on this bucket, copy the following bucket policy, and paste it in the Bucket policy editor.
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/editpolicy.PNG)
### step 6 - Go back to cloudfront and access the distribution 
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/finalstep.PNG)
## The URL for the distribution can be found under the Domain name column.you will see your static website by accessing this URL on your web browser.
![installation1](https://github.com/Ayomide26/Aws-Task1/blob/main/images/finalstep1.PNG)

