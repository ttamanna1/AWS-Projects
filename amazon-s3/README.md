# Hosting A Website On Amazon S3

### What is Amazon s3?
Amazon S3 (Simple Storage Service) is an object storage service that is
designed to store and retrieve any amount of data at anytime from anywhere on
the web.

### How I used Amazon S3 in this project
I created a static HTML calculator website using Tailwind CSS for styling. This project was very quick and beginner friendly. Requires an AWS account.

## How I Set Up an S3 Bucket
Creating an S3 bucket is very quick. 
1. Login to AWS. 
2. In the Management Console of my AWS account, I searched for S3. 
3. The Region I picked for my S3 bucket was Europe (London) eu-west-2 becasue
that Region is the closest to my location.
4. Choose **Create bucket**.
5. For **Bucket name**, I chose 'calculator-s3-project'. S3 bucket names are globally unique. This means that no other AWS account in the entire world have the same bucket name as mines (unless I delete the
bucket).
6. For **Object Ownership**, I chose **ACLs enabled** and **Bucket owner preferred**. An ACL (access control list) is a set of rules that decides who can get access to
a resource. Enabling ACLs in S3 lets you control who can access and do things
with the objects you upload into your bucket.
7. For **Block Public Access settings for this bucket**, I unchecked the **Block all public access** checkbox.
8. I checked the box that says **“I acknowledge that the current settings might result in this bucket and the objects within becoming public.”**
9. For **Bucket Versioning**, I chose **Enabled**.
10. **Create bucket**

![Bucket](/src/bucket-creation.png)

## Upload Website Files to S3
I uploaded two files to my S3 bucket - they were an index.html file and an
output.css file. Both files are necessary for this project as the index.html file will display my
website and the output.css file is the styles I want my website to display.
1. In the **Objects** tab of my S3 bucket, I selected **Upload**.
2. I selected **Add files** and uploaded my index.html file and output.css file.
3. **Upload**

![File-Uploads](/src/file-uploads.png)

## Static Website Hosting on S3
Web hosting means storing your HTML file (and the other files for your website)
on a web server, so it's accessible online.
1. In my buckets page, I selected the **Properties** tab.
2. I scrolled down to the **Static website hosting** panel.
3. I selected **Edit**.
4. For **Static web hosting**, I selected **Enable**.
5. For **Hosting type**, I chose **Host a static website**.
6. For **Index document**, I entered index.html.
7. **Save changes**.

![Static-Website-Hosting](/src/static-website-hosting.png)

## Bucket Endpoints
Once static website is enabled, S3 produces a bucket endpoint URL, which is
just like a regular website URL. It lets people visit your S3 bucket as a website. In the **Static website hosting** panel, I clicked on the URL under **Bucket website endpoint**. I saw an error message '403
Forbidden' on the webpage. The reason for this error was that my objects in my
bucket are private by default. This default setting helps keep my account's data
secure.

![Error](/src/error.png)

To resolve this connection error:
1. I selected my files under the **Objects** tab.
2. Clicked on **Actions**.
3. Selected **Make public using ACL**.
4. Refresh URL webpage. 

![Calculator-Webpage](/src/s3-website.png)

### Deleting Resources
To avoid any charges for this project, I deleted my bucket.