# AWS_Add-a-CI-CD-pipeline-to-an-Amazon-S3-bucket

<h2>CI/CD pipeline to an Amazon S3 bucket.</h2>

Following the steps you should follow


Step 1: Go to the AWS console.<br><br>
Step 2: Search for S3 and open it.<br><br>
Step 3: Now we are creating S3 buckets.<br><br>
Step 4: So for that, click on "Create bucket."<br><br>
Step 5: Enter the name of the bucket. <br><br>
Step 6: Select a region.<br><br>
Step 7: In Object Ownership, we have two options.<br>
1. ACLs disabled.<br>
2. ACLs enabled.<br><br>

Step 8: We select "ACLs enabled."<br><br>
Step 9: Then scroll down, and we see Block Public Access settings.<br><br>
Step 10: So in this, we uncheck the checkbox because we want access to a public IP.<br>
**Note:** Click on Acknowledge Note.<br><br>
Step 11: For noe in bucket versioning, we select "Disable."<br><br>
Step 12: In default encryption, we select "Disable."<br><br>
Step 13: Then click on "create bucket."<br><br>
Step 14: Now your bucket is ready.<br><br>
Step 15: Now we see some options like Actions, Create folder, and Upload.<br><br>
Step 16: We click on "Upload."<br><br>
Step 17: Then click on Add file or Add folder.<br><br>
Step 18: Then click on upload.<br><br>
Step 19: Now, in our bucket, we see our files.<br><br>
Step 20: In the bucket, we see many different fields like Object, Properties, Permissinons, Metrics, Management and Access Points.<br><br>
Step 21: Now we are clicking on Properties.<br><br>
Step 22: Scroll down and click on static website hosting; click on "Edit."<br><br>
Step 23: Enable this option.<br><br>
Step 24: Scroll down and, in the index document, write your file name (which is important in my case; index.html is important).<br><br>
Step 25: Now click on "Save changes."<br><br>
Step 26: Now we click on permissions.<br><br>
Step 27: Click on Bucket Policy and click on "Edit."<br><br>
Step 28: Here we create a policy for buckets.<br><br>
Step 29: Then click on "Save changes."<br><br>
Step 30: Again, we go to the Properties.<br><br>
Step 31: Now scroll down and click on static website hosting. AWS gives you a URL for your website, so click on it.<br><br>
Step 32: Now we are going to create a CI/CD pipeline.<br><br>
Step 33: For that Open your AWS console dashboard.<br><br>
Step 34: Search CodePipeline; open it.<br><br>
Step 35: Enter the name of the pipeline.<br><br>
Step 36: In the service role, we have two options.<br><br>
1. New service role.<br>
2. Existing service roles.<br>
Step 37: Now click on "Next."<br><br>
Step 38: Now select your pipeline Source.<br>
We see many options.<br>
• Aws CodeCommit.<br>
• Amazon ECR.<br>
• Amazon S3.<br>
• BitBucket.<br>
• GitHub (Version 1).<br>
• GitHub (Version 2).<br>
• GitHub Enterprise Server.<br><br>
Step 39: We select "GitHub (Version 2)"<br><br>
Step 40: Now click on "Connect to Github."<br><br>
Step 41: Now we are creating a connection page.<br><br>
Step 42: Enter the name of the Connection.<br><br>
Step 43: Click on "Connect to GitHub."<br><br>
Step 44: Then click on Install a New App.<br><br>
Step 45: Before that, go to GitHub.com to give access to AWS.<br><br>
Step 46: Then give repository access; click on save.<br><br>
Step 47: Now, in the AWS console, we see the Connect to GitHub page.<br><br>
Step 48: Click on Connect.<br><br>
Step 49: Now in the Source stage.<br><br>
Step 50: In the repository name, we see automatically that our repo has come.<br><br>
Step 51: Select the branch name.<br><br>
Step 52: Click on "next."<br><br>
Step 53: Now we can see the Build Stage page.<br><br>
Step 54: For now, we skip.<br><br>
Step 55: Now we can see Deploy stage page.<br><br>
Step 56: Deploy the provider. <br><br>
Step 57: We can see many fields like AWS AppConfig, AWS ClounFormation, AWS ClounFormation Stack Set, AWS CodeDeploy, AWS Elastic Beanstalk, AWS OpsWorks Stack, AWS Service Catalog, Alexa Skills Kit, Amazon ECS, Amazon ECS (Blue/Green), and Amazon S3.<br><br>
Step 58: Here we select Amazon S3.<br><br>
Step 59: In Deployment path, we write "static/".<br><br>
Step 60: Click on the checkbox for Extract File before deploying.<br><br>
Step 61: Click on Next.<br><br>
Step 62: Now that we are on the review page, scroll down and click on Create Pipeline.<br><br>
Step 63: Now our pipeline is almost done, and it's ready. <br><br>
Step 64: Go to the S3 bucket and click on your bucket.<br><br>
Step 65: Then click on "static/"<br><br>
Step 66: Follow this step: "static/" -> "/" -> "Code.Upload.txt.<br><br>
Step 67: In that, we see all the details.<br><br>
Step 68: Now open hour github.<br><br>
Step 69: So that you can verify whether your code is deployed or not.<br><br>
Step 70: Go to S3 Bucket, open our bucket, and go to "static/" -> "/" -> "Code.Upload.txt. <br><br>
Step 71: Then we see the URL of our bucket.<br><br>
Step 72: Now our pipeline is done and our code is deployed.<br><br>
