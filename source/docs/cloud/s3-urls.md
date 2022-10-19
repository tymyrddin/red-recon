# Investigating S3 URLs

## Endpoints

`S3 endpoint` is a region-specific URL that is used in both S3 URL styles. 

Most of the endpoints follow this pattern (with region names being `eu-west-1`, `us-west-2`, etc):

    s3-REGION.amazonaws.com

And there are some oddities to know.

Two endpoints that do not follow the above pattern are those of the `us-east-1` region. 
For that region endpoints are synonyms and both point to the same place:

    s3.amazonaws.com
    s3-external-1.amazonaws.com

Further, the `eu-central-1` (Frankfurt) and `ap-northeast-2` (Seoul) regions both have one endpoint 
that follows the general pattern and one alias endpoint that differs from the general scheme in one symbol 
(the first dash is replaced by dot):

    s3-eu-central-1.amazonaws.com
    s3.eu-central-1.amazonaws.com

    s3-ap-northeast-2.amazonaws.com
    s3.ap-northeast-2.amazonaws.com

## S3 bucket URL schemes

According to the S3 Developer Guide (PDF, p.57), S3 supports both virtual-hosted and path URL styles for bucket access.

## Path style URL

In path style URL, the bucket name is appended to the domain name and is a part of the URL path:

    http://s3endpoint/<bucket-name>

## Virtual-hosted style URL

In virtual-hosted style URL the bucket name becomes a subdomain:

    http://BUCKET.s3endpoint

## Static Website Hosting Endpoints

Using S3's Static Website Hosting feature requires using Website Endpoints.

There are two general forms of S3 website endpoint:

    http://BUCKET.s3-website-region.amazonaws.com
    http://BUCKET.s3-website.region.amazonaws.com

Most of the regions follow the first form, while `eu-central-1` and `ap-northeast-2` follow the second. 