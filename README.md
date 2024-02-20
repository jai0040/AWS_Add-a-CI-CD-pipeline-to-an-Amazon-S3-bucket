# AWS_Add-a-CI-CD-pipeline-to-an-Amazon-S3-bucket

Add a CI/CD pipeline to an Amazon S3 bucket.


Following the steps you should follow


Step 1: Go to the AWS console.
Step 2: Search for S3 and open it.
Step 3: Now we are creating S3 buckets.
Step 4: So for that, click on "Create bucket."
Step 5: Enter the name of the bucket. 
Step 6: Select a region.
Step 7: In Object Ownership, we have two options.
1. ACLs disabled.
2. ACLs enabled.
Step 8: We select "ACLs enabled."
Step 9: Then scroll down, and we see Block Public Access settings.
Step 10: So in this, we uncheck the checkbox because we want access to a public IP.
Note: Click on Acknowledge Note.
Step 11: For noe in bucket versioning, we select "Disable."
Step 12: In default encryption, we select "Disable."
Step 13: Then click on "create bucket."
Step 14: Now your bucket is ready.
Step 15: Now we see some options like Actions, Create folder, and Upload.
Step 16: We click on "Upload."
Step 17: Then click on Add file or Add folder.
Step 18: Then click on upload.
Step 19: Now, in our bucket, we see our files.
Step 20: In the bucket, we see many different fields like Object, Properties, Permissinons, Metrics, Management and Access Points.
Step 21: Now we are clicking on Properties.
Step 22: Scroll down and click on static website hosting; click on "Edit."
Step 23: Enable this option.
Step 24: Scroll down and, in the index document, write your file name (which is important in my case; index.html is important).
Step 25: Now click on "Save changes."
Step 26: Now we click on permissions.
Step 27: Click on Bucket Policy and click on "Edit."
Step 28: Here we create a policy for buckets.
Step 29: Then click on "Save changes."
Step 30: Again, we go to the Properties.
Step 31: Now scroll down and click on static website hosting. AWS gives you a URL for your website, so click on it.
Step 32: Now we are going to create a CI/CD pipeline.
Step 33: For that Open your AWS console dashboard.
Step 34: Search CodePipeline; open it.
Step 35: Enter the name of the pipeline.
Step 36: In the service role, we have two options.
1. New service role.
2. Existing service roles.
Step 37: Now click on "Next."
Step 38: Now select your pipeline Source.
We see many options.
• Aws CodeCommit.
• Amazon ECR.
• Amazon S3.
• BitBucket.
• GitHub (Version 1).
• GitHub (Version 2).
• GitHub Enterprise Server.
Step 39: We select "GitHub (Version 2)"
Step 40: Now click on "Connect to Github."
Step 41: Now we are creating a connection page.
Step 42: Enter the name of the Connection.
Step 43: Click on "Connect to GitHub."
Step 44: Then click on Install a New App.
Step 45: Before that, go to GitHub.com to give access to AWS.
Step 46: Then give repository access; click on save.
Step 47: Now, in the AWS console, we see the Connect to GitHub page.
Step 48: Click on Connect.
Step 49: Now in the Source stage.
Step 50: In the repository name, we see automatically that our repo has come.
Step 51: Select the branch name.
Step 52: Click on "next."
Step 53: Now we can see the Build Stage page.
Step 54: For now, we skip.
Step 55: Now we can see Deploy stage page.
Step 56: Deploy the provider. 
Step 57: We can see many fields like AWS AppConfig, AWS ClounFormation, AWS ClounFormation Stack Set, AWS CodeDeploy, AWS Elastic Beanstalk, AWS OpsWorks Stack, AWS Service Catalog, Alexa Skills Kit, Amazon ECS, Amazon ECS (Blue/Green), and Amazon S3.
Step 58: Here we select Amazon S3.
Step 59: In Deployment path, we write "static/".
Step 60: Click on the checkbox for Extract File before deploying.
Step 61: Click on Next.
Step 62: Now that we are on the review page, scroll down and click on Create Pipeline.
Step 63: Now our pipeline is almost done, and it's ready. 
Step 64: Go to the S3 bucket and click on your bucket.
Step 65: Then click on "static/"
Step 66: Follow this step: "static/" -> "/" -> "Code.Upload.txt.
Step 67: In that, we see all the details.
Step 68: Now open hour github.
Step 69: So that you can verify whether your code is deployed or not.
Step 70: Go to S3 Bucket, open our bucket, and go to "static/" -> "/" -> "Code.Upload.txt. 
Step 71: Then we see the URL of our bucket.
Step 72: Now our pipeline is done and our code is deployed.
