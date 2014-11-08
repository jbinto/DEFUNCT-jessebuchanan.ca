# jessebuchanan.ca

## What?

This is the source code for Jesse Buchanan's website: http://jessebuchanan.ca

## How?

Usage:

Clone the repo.

    git clone git@github.com:jbinto/jessebuchanan.ca.git
    cd jessebuchanan.ca
   
Install the s3_website gem via bundler:

    bundle install


Set the AWS credentials. **NOTE:** Use a restricted IAM role for this!

    cp set_aws_credentials.sh.example set_aws_credentials.sh
    vi set_aws_credentials.sh
    source set_aws_credentials.sh

Push the website. s3_website knows to automagically deploy from `_site` (magic intended for Jekyll sites; this is not one).

    s3_website push


