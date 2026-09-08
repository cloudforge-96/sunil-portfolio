# AWS Portfolio Website

Static, dependency-free portfolio ready for Amazon S3 + CloudFront.

## Personalize before deployment

1. In `index.html`, replace `SK`, `Your Name`, and `your.email@example.com`.
2. Add your real experience dates, employer details, project links, and completed certifications.
3. The included `bhukya-sunil-kumar-naik-resume.pdf` is linked to the resume button. Replace it with an updated PDF when needed, keeping the same filename.

## Deploy to S3 + CloudFront

1. Create an S3 bucket and upload all files in this folder (including `style.css` and `script.js`).
2. Create a CloudFront distribution with the bucket as origin and set `index.html` as the default root object.
3. For private S3 access, use CloudFront Origin Access Control (OAC); do not make the bucket public.
4. If using a domain, add it to CloudFront and create the Route 53 alias record.

For CloudFront updates, create an invalidation for `/*` after uploading changed files.
