# AWS Keypair Terraform Module 

A Terraform module which will create a keypair used to connected to EC2 instances.

This type of resource is supported :
- [KEYPAIR - aws_key_pair](https://www.terraform.io/docs/providers/aws/r/key_pair.html)

# Features

The goal of this module is to create a public key that will be used to connect to EC2 instances. 
It will not create a key for you as you need to specify the publi key that you want to use.
The module supports :

- keypair name
- public_key

## Terraform versions

Support of Terraform 0.12 is not yet implemented. (WIP)

If you are using Terraform 0.11 you can use versions `v1.*`.

## Usage

Public Key Pair creation example: 

```hcl
module "aws_key_pair" {
  source     = "app.terraform.io/<ORG_NAME>/keypair/aws"
  key_name   = "rhforum-2019-key"
  public_key = "ssh-rsa ..."
}
```

## Authors

* **Nicolas Ehrman** - *Initial work* - [Hashicorp](https://www.hashicorp.com)



