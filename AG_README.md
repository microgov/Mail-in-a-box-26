AG
---
 - NEW VERSION IN PROGRES
 - https://github.com/microgov/Mail-in-a-box-26
 - using this miaB fork as upsteam source
 - https://github.com/LM1337/Mail-in-a-box-26

---
Mail in a box for AWS Cloud Formation

requires companion template.yaml file to launch stack


instruction
reference tuts

https://github.com/mmeidlinger/aws-opensource-mailserver

https://github.com/mmeidlinger/mailinabox

https://gist.github.com/CameronGuthrie/347fa812cb52853fe7aefa0a2ad67341

https://github.com/aws-samples/aws-opensource-mailserver

https://github.com/aws-samples/aws-opensource-mailserver/blob/main/README.md

Preliminary steps: Setting up DNS and creating S3 Buckets
1. Allocate an Elastic IP address
2. Configure DNS
3. Create S3 buckets for backups and user data
all before launching stack

included cloud formation stack template.yaml file
does not create the s3 buckets nor does it allocate the elastic ip