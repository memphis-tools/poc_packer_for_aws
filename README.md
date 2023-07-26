![Screenshot](hashicorp-packer.svg)
# POC Hashicorp Packer for AWS

## What is it ?
Just a basic dummy POC for a Packer usage when creating a Linux based AMI.

Instance type is a t2.micro free tier, region eu-west-3. Ubuntu image based.

## Useful Links:
https://github.com/hashicorp/packer

https://developer.hashicorp.com/packer/tutorials/aws-get-started/aws-get-started-build-image

https://access.redhat.com/solutions/15356

https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html-single/composing_a_customized_rhel_system_image/index#creating-cloud-images-with-composer_composing-a-customized-rhel-system-image

## How use this ?
`git clone https://github.com/memphis-tools/poc_packer_for_aws.git`

`cd poc_packer_for_aws`

Actually, you just need to follow https://developer.hashicorp.com/packer/tutorials/aws-get-started/aws-get-started-build-image

Initialize your Packer configuration.

`packer init .`

Format and validate your Packer template.

`packer fmt .`

`packer validate .`

Export your AWS keys.

`export AWS_ACCESS_KEY_ID="xxx"`

`export AWS_SECRET_ACCESS_KEY="yyy"`

Build Packer image.

`packer build aws-ubuntu.pkr.hcl`
