# My Take
This project is almost perfect for S3 hosting, as it's a simple static site, extremely cheap to run and since its essentially serverless it wont need monitoring, however, metrics will be available in cloudwatch.

Apologies if the commits are weird, I'm using the github web console and manually uploading files there.

# Task
- Deploy the provided static page to AWS

- The page should be publicly accessible

- Build a deployment pipeline in AWS, so updates to the master branch are
automatically reflected on the site

- Use Infrastructure as code to build any required infrastructure (preferabbly
CloudFormation but terraform is also acceptable)

- Commit to your project frequently to show how you are approaching the task

# Points to consider when architecting the solution
- Scalability - Its an S3 bucket, it wont need to scale. Here is one that took 3.5 million requests in a day! - https://www.digital-web.com/articles/scalable-hosting-s3/

- Availitibily - AWS says S3 should have 99.99% uptime, which is 52mins downtime a year. I think this should be acceptable.

- Disaster Recovery - S3 is automatically stored accross 3 AZ's per reigon, meaning it should be fairly reliable.

- Deployments - I shall make a pipeline in the cloudformation template

- Testing - due to the simplicity of this, I'm confident it wont need any testing, as long as it works.

- Costs - S3 is incredibly cheap

- Security - The bucket is open, which is a little scary, but since it's only hosting assets used on the site i think it's acceptable.

- Monitoring - Can be monitored via cloudwatch, and can have logs enabled on the bucket if need be.
