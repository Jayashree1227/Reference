# AWS CLI COMMANDS

## SETUP AWS CLI
To use AWS CLI, first download and install AWS CLI for windows 

## CONFIGURE KEYS

To configure private key and access key

> aws configure

* Default region: us-east-1
* Default Output Format: table

## AWS S3 BUCKETS

* > aws s3 ls -> lists all buckets
* > aws s3 mb s3://nov12-5-test -> Create a new bucket with the name nov12-5-test
* > aws s3 ls s3://land.giftsweep.us -> To find all the files inside the bucket land.giftsweep.us
* > aws s3 cp index.html s3://nov12-5-test -> copy a local file named index.html to the bucket nov12-test
* > aws s3 cp s3://nov12-5-test/index.html . -> copy index.html from s3 bucket to local (Note: There is a dot (.) after index.html)
