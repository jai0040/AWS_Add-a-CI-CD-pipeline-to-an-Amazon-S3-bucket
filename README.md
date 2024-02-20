# AWS_Add-a-CI-CD-pipeline-to-an-Amazon-S3-bucket


Add a CI/CD pipeline to an Amazon S3 bucket

Following the steps you should follow

Step 1: Go to the aws console.
Step 2: Search S3 and open it.
Step 3: Now we are create S3 Buckets.
Step 4: SO for that click on "Create bucket".
Step 5: Enter name of bucket. 
Step 6: Select region.
Step 7: In Object Ownership we have two options.
	1. ACLs disabled.
	2. ACLs enabled.
Step 8: We select "ACLs enabled".
Step 9: Then scroll down and we see Block Publick Access settings.
Step 10: So in this we uncheck the checkbox beacuse we want access of public ip.
Note : Click on Acknowledge note.
Step 11: For noe in Bucket versioning we select "Disable."
Step 12: I Default encryption we select "Disable."
Step 13: Then click on "creat bucket."
Step 14: Now your bucket is ready.
Step 15: Now we see some options like Actions, Create folder , Upload.
Step 16: We click on "Upload."
Step 17: Then click on Add file/ Add folder.
Step 18: Then click on upload.
Step 19: Now in our bucket we see our files.
Step 20: In bucket we see many diffrent fields like Object, Properties, Permissinons, Metrics, Management, Access Points.
Step 21: Now we are click on Properties.
Step 22: Scroll down and click on static website hosting; click on "Edit".
Step 23: Enable this option.
Step 24: Scroll down and In Index document write your file name(which is importante in my case index.html is importante.)
Step 25: Now click on "Save changes"
Step 26: NOw we click on Permissinons.
Step 27: Click on Bucket policy and click on "Edit".
Step 28: Now here we create policy for bucket.
Step 29: Then click on "Save changes".
Step 30: Again we go to the Properties.
Step 31: Now scroll down and click on static website hosting AWS give you URL for your website; so that click on it.
Step 32: Now we are going to create CI/CD pipeline.
Step 33: For that Open your AWS console dashbord.
Step 34: Search CodePipeline; Open it.
Step 35: Enter name of pipeline.
Step 36: In service role we have two options.
	1. New service role.
	2. Existinf service role.
Step 37: Now click on "Next"
Step 38: Now select your pipeline Source.
We see many options.
> Aws CodeCommit.
> Amazon ECR.
> Amazon S3.
> BitBucket.
> GitHub (Version 1).
> GitHub (Version 2).
> GitHub Enterprise Server.
Step 39: We select "GitHub (Version 2)"
Step 40: Now click on "Connect to Github."
Step 41: Now we are Create a connection page.
Step 42: Enter name of Connection.
Step 43: Click on "Connect to GitHub"
Step 44: Then click on install a new app.
Step 45: Before that go to the GitHub.com for give access to AWS.
Step 46: Then give repository access; click on save.
Step 47: Now in AWS console we see connect to github page.
Step 48: Click on connect.
Step 49: Now in Souce stage.
Step 50: In repository name we see automatically our repo come.
Step 51: Select branch name.
Step 52: Click on "next".
Step 53: Now we can see Build stage page.
Step 54: For now we skip.
Step 55: Now we can see Deploy stage page.
Step 56: Deploy provider 
Step 57: We can see many field like AWS AppConfig, AWS ClounFormation, AWS ClounFormation Stack Set, AWS CodeDeploy, AWS Elastic Beanstalk, AWS OpsWorks Stack, AWS Service Catalog, Alexa Skills Kit, Amazon ECS, Amazon ECS (Blue/Green), Amazon S3.
Step 58: Here we select Amazon S3.
Step 59: In Deployment path we write "static/".
Step 60: Click on checkbox for Extract file befor deploy.
Step 61: Click on next.
Step 62: Now we are on review page scroll down and click on create pipeline.
Step 63: Now our pipeline is almost done deplay and it's ready 
Step 64: Go to the S3 bucket and click on your bucket.
Step 65: Then click on "static/"
Step 66: Follow this step "static/" -> "/" -> "Code.Upload.txt .
Step 67: In that we see all the details.
Step 68: Now open hour github.
Step 69: So that you can verify your code is deploy or not.
Step 70: Go to S3 Bucket open our bucket and go to "static/" -> "/" -> "Code.Upload.txt 
Step 71: Then we see URL of our bucket.
Step 72: Now our pipeline is done and our code is deploy.
