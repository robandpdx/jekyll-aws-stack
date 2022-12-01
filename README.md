# jekyll-aws-stack

## Why should you use this stack?
So you want to create a [Jekyll](https://jekyllrb.com/) static website and host it in [AWS](https://aws.amazon.com/) with SSL. Well, to make this all happen you need to configure the following [AWS](https://aws.amazon.com/) services: [Route53, S3](https://aws.amazon.com/route53/), [CloudFront](https://aws.amazon.com/cloudfront/), [AWS Certificate Manager](https://aws.amazon.com/certificate-manager/), [Lambda](https://aws.amazon.com/lambda/). That's a bit overwhelming, just for a simple static website!

This project solves all of this by providing an [AWS sam](https://aws.amazon.com/serverless/sam/) template that sets up all the necessary infrastructure for serverless web hosting on AWS. There is also a [GitHub actions workflow](https://github.com/features/actions) to setup continuous delivery. The stack deploys the following:

- S3 bucket to host the static web files
- CloudFront distribution so you can add an SSL/TLS certificate
- SSL/TLS certificate
- Route53 record in your hosted zone
- Edge lamda for better SEO

## Prerequisites
- [AWS account](https://aws.amazon.com/)
- [Hosted zone in Route53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/CreatingHostedZone.html)

## What are the inputs to pass while setting up the stack?
```
- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- DOMAIN_NAME
- HOST_NAME
- HOSTED_ZONE_ID
```
