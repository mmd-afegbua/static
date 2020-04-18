# static

### Static is a Jenkins Pipeline (Blue Ocean) Project on AWS

#### Requirements:
* AWS Root Account - Yeah!
* AWS User
    * Group with AmazonEC2FullAccess, AmazonVPCFullAccess, Amazons3FullAccess
    * IAM User with Login credentials, ID and private key
* Jenkins Server on EC2: Ubuntu 18.04 f1.micro freetier - your choice.
Follow these steps to install jenkins on your instance: https://aws.amazon.com/getting-started/hands-on/setup-jenkins-build-server/
* s3 Bucket
* Githun Repo
* Install Tidy on your server: https://zoomadmin.com/HowToInstall/UbuntuPackage/tidy 

#### Required Jenkins Plugins
1. Blue Ocean
2. Pipeline AWS
3. AWS Credentials Plugin

#### To create the pipeline
Clone this repo by using the command: ```git clone https://github.com/mmd-afegbua/static.git```

