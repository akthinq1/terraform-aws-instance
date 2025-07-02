# 🖥️ Terraform EC2 Module

This Terraform module provisions an **EC2 instance** in AWS with customizable parameters like AMI ID, instance type, tags, and Security Group ID. It outputs useful details like the instance's public IP, private IP, and instance ID.


## 🔧 Input Variables

| Name           | Description                          | Type     | Required |
|----------------|--------------------------------------|----------|----------|
| `ami_id`       | AMI ID to launch the EC2 instance    | `string` | ✅ Yes   |
| `instance_type`| Type of EC2 instance (e.g., t2.micro)| `string` | ✅ Yes   |
| `tags`         | Tags to apply to the instance        | `map`    | ❌ No    |
| `sg_id`        | Security Group ID to attach          | `string` | ✅ Yes   |

---

## 📤 Outputs

| Name             | Description                      |
|------------------|----------------------------------|
| `public_ip`      | Public IP of the EC2 instance     |
| `private_ip`     | Private IP of the EC2 instance    |
| `instance_id`    | ID of the EC2 instance            |

---

AWS EC2 instance
You can create EC2 instance in joindevops using this module

Inputs
ami_id(Optional) - AMI ID that need to be used by instance. Default is devops-practice i.e ami-09c813fb71547fc4f
instance_type (Optional) - Instance type to be used by instance. Valid values are t3.micro, t3.small. t3.medium. Default is t3.micro
sg_ids (Required) - A list of Security Group IDS to attach instance
tags (Required) - A map of tags to be associated with instance
Outputs
public_ip - Public IP of the instance created
private_ip - Private IP of the instance created
instance_id - Instance ID of the instance created