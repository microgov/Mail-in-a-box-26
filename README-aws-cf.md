# Mail-in-a-Box for AWS CloudFormation (Ubuntu 26.04)

> **Status:** Work in Progress  
> **Repository:** [microgov/Mail-in-a-box-26](https://github.com/microgov/Mail-in-a-box-26) (branch: `aws-cf`)  
> **Upstream Fork:** [LM1337/Mail-in-a-box-26](https://github.com/LM1337/Mail-in-a-box-26)

This guide covers deploying the Ubuntu 26.04 fork of Mail-in-a-Box on AWS using the companion `template.yaml` CloudFormation stack.

---

## Preliminary Steps (Required Before Launching Stack)

The included CloudFormation `template.yaml` **does not** create S3 buckets or allocate an Elastic IP. Complete these steps manually before deploying the stack:

1. **Allocate an Elastic IP Address:** Reserve a static public IPv4 address in EC2 so your mail server's IP persists across instance replacements. *(Remember to request AWS reverse DNS / PTR record updates and port 25 unblocking if needed.)*
2. **Configure DNS:** Point your domain's glue records (`ns1.box.yourdomain.com`, `ns2.box.yourdomain.com`) to your new Elastic IP at your domain registrar.
3. **Create S3 Buckets:** Create dedicated S3 buckets for Mail-in-a-Box encrypted backups and user data.

---

## Reference Tutorials & Sources

* [aws-samples/aws-opensource-mailserver](https://github.com/aws-samples/aws-opensource-mailserver) ([README](https://github.com/aws-samples/aws-opensource-mailserver/blob/main/README.md))
* [mmeidlinger/aws-opensource-mailserver](https://github.com/mmeidlinger/aws-opensource-mailserver)
* [mmeidlinger/mailinabox](https://github.com/mmeidlinger/mailinabox)
* [CameronGuthrie's Mail-in-a-Box AWS Gist](https://gist.github.com/CameronGuthrie/347fa812cb52853fe7aefa0a2ad67341)
