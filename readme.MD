# 🖥️ Terraform EC2 Module

This Terraform module provisions an **EC2 instance** in AWS with customizable parameters like AMI ID, instance type, tags, and Security Group ID. It outputs useful details like the instance's public IP, private IP, and instance ID.


## 🔧 Input Variables

| Name           | Description                          | Type     | Required |
|----------------|--------------------------------------|----------|----------|
| `ami_id`       | AMI ID to launch the EC2 instance    | `string` | ✅ Yes   |
| `instance_type`| Type of EC2 instance (e.g., t2.micro)| `string` | ✅ Yes   |
| `tags`         | Tags to apply to the instance        | `map`    | ✅ Yes   |
| `sg_id`        | Security Group ID to attach          | `string` | ✅ Yes   |

---

## 📤 Outputs

| Name             | Description                      |
|------------------|----------------------------------|
| `public_ip`      | Public IP of the EC2 instance     |
| `private_ip`     | Private IP of the EC2 instance    |
| `instance_id`    | ID of the EC2 instance            |

---

