# keboola-academy

[![Build Status](https://travis-ci.org/keboola/keboola-academy.svg?branch=master)](https://travis-ci.org/keboola/keboola-academy)

Static website for academy.keboola.com


### Deployment

Website is hosted in AWS S3 bucket behind AWS Cloudfront CDN with custom domain and forced https.
AWS resources are provided by [Cloudformation stack](https://github.com/keboola/keboola-academy/blob/master/cf-stack.json):
- S3 Bucket - bucket where the page assets are stored
- CDN distribution
- Deploy Policy - policy providing write permissions to created S3 bucket
- Deploy Group - group with deploy policy attached

New release is published (uploaded to S3) after each push to `master` branch. 

**Notice** There is a `5 minutes` HTTP cache, so changes may not occur immediately.

