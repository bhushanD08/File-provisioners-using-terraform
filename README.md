# File Provisioners using Terraform

This repository demonstrates how to use Terraform provisioners to automate setup tasks on AWS EC2 instances.

It contains examples for:

- `file` provisioner
- `local-exec` provisioner
- `remote-exec` provisioner

## Overview

Terraform provisioners are used to perform actions on a resource after it is created. These examples show common patterns for:

- copying files to an EC2 instance
- running commands locally on the machine where Terraform is executed
- running commands remotely on the provisioned instance over SSH

## Repository Structure

- `File-provisoner/` – example using the `file` provisioner
- `Local-Provisoner/` – example using the `local-exec` provisioner
- `Remote-provisoner/` – example using the `remote-exec` provisioner
- `index.html` – sample HTML file used as a demo asset

## Prerequisites

Before running the Terraform examples, make sure you have:

- Terraform installed
- AWS CLI configured with valid credentials
- An AWS account with permissions to create EC2 resources
- A valid SSH key pair or configuration for EC2 access

## Example Details

### 1. File Provisioner
Location: `File-provisoner/`

This example copies a file from a local machine to an EC2 instance using a `file` provisioner.

### 2. Local Provisioner
Location: `Local-Provisoner/`

This example uses `local-exec` to run a command on the system where Terraform is executing, such as writing instance metadata to a local file.

### 3. Remote Provisioner
Location: `Remote-provisoner/`

This example uses `remote-exec` to install and configure software on the EC2 instance after it boots, such as installing NGINX and writing a simple web page.

## How to Use

From any example directory:

```bash
terraform init
terraform validate
terraform plan
terraform apply
```

After deployment, you can destroy the resources:

```bash
terraform destroy
```

## Notes

- The examples are intended for learning and demonstration purposes.
- You may need to update variables such as AMI ID, subnet ID, instance type, and SSH key paths to match your AWS environment.
- Some configuration values are hardcoded in the example files and can be customized as needed.

## License

This project is provided for educational purposes.

## Author

Bhushan D. 
