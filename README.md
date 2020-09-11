# Course: Essential Google Cloud Infrastructure: Foundation
 The Course introduces us   a  comprehensive and flexible infrastructure and platform services provided by Google Cloud with a focus on Compute Engine
# LAB 1 : Console and Cloud Shell

- step 1: (open )[https://console.cloud.google.com]
- step 2 : login with your account
- step 3 : Create  project in your cloud console dashboard
- step 4 : launch the cloud shell  or Open a terminal window
Using the gsutil mb command and a unique name to create a bucket

```
gsutil mb -b on -l us-central1 gs://my-bucket

```
to Upload a file
Click Upload file. Upload any file from your local machine to the Cloud Shell VM. This file will be referred to as [MY_FILE].

In Cloud Shell, type ls to confirm that the file was uploaded
Copy the file into one of the buckets you created earlier in the lab. Replace [MY_FILE] with the file you uploaded and [BUCKET_NAME] with one of your bucket names:

 ``` gsutil cp [MY_FILE] gs://[BUCKET_NAME] ```
execute to list regions
``` gcloud compute regions list ```

environment variable and replace [YOUR_REGION] with the region you selected in the previous step
``` INFRACLASS_REGION=[YOUR_REGION] ```

Verify it with echo

``` echo $INFRACLASS_REGION ```

Append the environment variable to a fileAppend the environment variable to a file
``` mkdir infraclass ```
Create a file called config
``` touch infraclass/config ```

 and Append the value of your Region environment variable to the config file
 ```echo INFRACLASS_REGION=$INFRACLASS_REGION >> ~/infraclass/config```
using source command to set the environment variables, and use the echo command to verify that the project variable was set
 ``source infraclass/config && echo $INFRACLASS_PROJECT_ID``

 enter ``` nano .profile``` to edit the shell profile
 Add the  ``` source infraclass/config ``` to the end of the file



# Lab 2 :