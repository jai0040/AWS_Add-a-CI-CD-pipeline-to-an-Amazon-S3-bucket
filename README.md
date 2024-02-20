# AWS_Add-a-CI-CD-pipeline-to-an-Amazon-S3-bucket


<H2>Add a CI/CD pipeline to an Amazon S3 bucket</H2>

Following the steps you should follow

Step 1: Go to the aws console.<br><br>
Step 2: Search S3 and open it.<br><br>
Step 3: Now we are create S3 Buckets.<br><br>
Step 4: SO for that click on "Create bucket".<br><br>
Step 5: Enter name of bucket. <br><br>
Step 6: Select region.<br><br>
Step 7: In Object Ownership we have two options.<br><br>
	1. ACLs disabled.
	2. ACLs enabled.
Step 8: We select "ACLs enabled".<br><br>
Step 9: Then scroll down and we see Block Publick Access settings.<br><br>
Step 10: So in this we uncheck the checkbox beacuse we want access of public ip.<br><br>
Note : Click on Acknowledge note.<br><br>
Step 11: For noe in Bucket versioning we select "Disable."<br><br>
Step 12: I Default encryption we select "Disable."<br><br>
Step 13: Then click on "creat bucket."<br><br>
Step 14: Now your bucket is ready.<br><br>
Step 15: Now we see some options like Actions, Create folder , Upload.<br><br>
Step 16: We click on "Upload."<br><br>
Step 17: Then click on Add file/ Add folder.<br><br>
Step 18: Then click on upload.<br><br>
Step 19: Now in our bucket we see our files.<br><br>
Step 20: In bucket we see many diffrent fields like Object, Properties, Permissinons, Metrics, Management, Access Points.<br><br>
Step 21: Now we are click on Properties.<br><br>
Step 22: Scroll down and click on static website hosting; click on "Edit".<br><br>
Step 23: Enable this option.<br><br>
Step 24: Scroll down and In Index document write your file name(which is importante in my case index.html is importante.)<br><br>
Step 25: Now click on "Save changes"<br><br>
Step 26: NOw we click on Permissinons.<br><br>
Step 27: Click on Bucket policy and click on "Edit".<br><br>
Step 28: Now here we create policy for bucket.<br><br>
Step 29: Then click on "Save changes".<br><br>
Step 30: Again we go to the Properties.<br><br>
Step 31: Now scroll down and click on static website hosting AWS give you URL for your website; so that click on it.<br><br>
Step 32: Now we are going to create CI/CD pipeline.<br><br>
Step 33: For that Open your AWS console dashbord.<br><br>
Step 34: Search CodePipeline; Open it.<br><br>
Step 35: Enter name of pipeline.<br><br>
Step 36: In service role we have two options.<br><br>
	1. New service role.
	2. Existinf service role.
Step 37: Now click on "Next"<br><br>
Step 38: Now select your pipeline Source.<br><br>
We see many options.<br><br>
> Aws CodeCommit.
> Amazon ECR.
> Amazon S3.
> BitBucket.
> GitHub (Version 1).
> GitHub (Version 2).
> GitHub Enterprise Server.
Step 39: We select "GitHub (Version 2)"<br><br>
Step 40: Now click on "Connect to Github."<br><br>
Step 41: Now we are Create a connection page.<br><br>
Step 42: Enter name of Connection.<br><br>
Step 43: Click on "Connect to GitHub"<br><br>
Step 44: Then click on install a new app.<br><br>
Step 45: Before that go to the GitHub.com for give access to AWS.<br><br>
Step 46: Then give repository access; click on save.<br><br>
Step 47: Now in AWS console we see connect to github page.<br><br>
Step 48: Click on connect.<br><br>
Step 49: Now in Souce stage.<br><br>
Step 50: In repository name we see automatically our repo come.<br><br>
Step 51: Select branch name.<br><br>
Step 52: Click on "next".<br><br>
Step 53: Now we can see Build stage page.<br><br>
Step 54: For now we skip.<br><br>
Step 55: Now we can see Deploy stage page.<br><br>
Step 56: Deploy provider <br><br>
Step 57: We can see many field like AWS AppConfig, AWS ClounFormation, AWS ClounFormation Stack Set, AWS CodeDeploy, AWS Elastic Beanstalk, AWS OpsWorks Stack, AWS Service Catalog, Alexa Skills Kit, Amazon ECS, Amazon ECS (Blue/Green), Amazon S3.<br><br>
Step 58: Here we select Amazon S3.<br><br>
Step 59: In Deployment path we write "static/".<br><br>
Step 60: Click on checkbox for Extract file befor deploy.<br><br>
Step 61: Click on next.<br><br>
Step 62: Now we are on review page scroll down and click on create pipeline.<br><br>
Step 63: Now our pipeline is almost done deplay and it's ready <br><br>
Step 64: Go to the S3 bucket and click on your bucket.<br><br>
Step 65: Then click on "static/"<br><br>
Step 66: Follow this step "static/" -> "/" -> "Code.Upload.txt .<br><br>
Step 67: In that we see all the details.<br><br>
Step 68: Now open hour github.<br><br>
Step 69: So that you can verify your code is deploy or not.<br><br>
Step 70: Go to S3 Bucket open our bucket and go to "static/" -> "/" -> "Code.Upload.txt <br><br>
Step 71: Then we see URL of our bucket.<br><br>
Step 72: Now our pipeline is done and our code is deploy.<br><br>
