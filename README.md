# Static-Web-Hosting

This project demonstrates how to host a static website using Amazon S3 bucket. The website includes an HTML page, an image, and a public read policy for S3 objects.

## Project Structure

- `INDEX.HTML1.txt`: Contains the HTML code for static website.
- `leopard.jpg.png`: Image used in the website.
- `S3 Bucket Policy.txt`: JSON policy to grant public read access to bucket objects.

## Steps to Host Static Website

1. Create an S3 Bucket
   - Name your bucket (e.g., `myfirstwebsite78610`).
   - Enable public access settings as required.

2. Upload Website Files
   - Upload `INDEX.HTML` and `leopard.jpg` to the S3 bucket.
   - Ensure files are named correctly.

3. Set Bucket Policy
   - Apply the following policy to allow public read of objects:
     ```
     {
         "Version": "2012-10-17",
         "Statement": [
             {
                 "Sid": "PublicReadGetObject",
                 "Effect": "Allow",
                 "Principal": "*",
                 "Action": "s3:GetObject",
                 "Resource": "arn:aws:s3:::myfirstwebsite78610/*"
             }
         ]
     }
     ```
4. Enable Static Website Hosting
   - Go to S3 bucket properties and enable static website hosting.
   - Set `INDEX.HTML` as the entry point.



