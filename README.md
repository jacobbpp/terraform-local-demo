# A Demonstration of Local Terraform

This repository provides a **clean, cloud-free introduction to Terraform**, perfect for learning the fundamentals of Infrastructure as Code (IaC) without needing AWS, Azure, or GCP credentials.

It’s designed for students, educators, and anyone new to Terraform who wants to explore:

## What You’ll Learn

This demonstration covers the **core lifecycle methods** in Terraform:

- `terraform init` – Initialises your project and downloads any required providers  
- `terraform validate` – Checks for syntax and configuration errors  
- `terraform plan` – Shows what Terraform *will do* before it does it  
- `terraform apply` – Provisions infrastructure (in this case, a simple local resource)

You’ll also understand the **structure of IaC projects**, including:

- **Providers** – These define *where* and *how* infrastructure will be provisioned  
- **Resources** – These are the *things* Terraform manages (servers, files, commands)  
- **Outputs** – These provide usable values from your infrastructure (e.g. IPs, URLs)

---

## Why This Is Useful

Infrastructure as Code is a key part of DevOps, but getting started often requires cloud access, credentials, and billing accounts. This project removes those barriers.

By using the `null_resource` and `local-exec` provisioner, you’ll:

- Learn how Terraform works **without provisioning anything in the cloud**  
- Focus entirely on Terraform’s workflow, language, and automation concepts  
- See how Terraform integrates seamlessly into a **CI pipeline** using GitHub Actions  
- Understand how pipelines automate infrastructure provisioning and change tracking

---

## How It Works

When you push changes to this repo:

1. GitHub Actions automatically runs the Terraform workflow
2. Terraform initialises the project
3. It validates the syntax
4. It plans what it will do (create a fake resource)
5. It applies that plan and runs a simple `echo` command

No cloud credentials, no bills, no risk, just the fundamentals.

---

## Great for Learning

This is an ideal starting point before progressing to:

- Cloud-based provisioning (AWS, Azure, GCP)
- Terraform modules and remote backends
- State management and collaboration practices
- Real-world DevOps pipelines that deploy live infrastructure

---

## 📂 Getting Started

To explore this locally:

```bash
git clone https://github.com/your-username/terraform-local-demo.git
cd terraform-local-demo
terraform init
terraform validate
terraform plan
terraform apply
```
You'll see a message like:
*Provisioning step complete – no cloud involved!*

---

## Want to Extend it?

Try adding:
- A second null_resource to simulate dependencies
- Outputs that return messages from your fake infrastructure
- A GitHub Actions job for terraform destroy
- PR triggers and approval steps to simulate production workflow

## Related Resources

- [Terraform Getting Started Guide](https://developer.hashicorp.com/terraform/tutorials)
- [GitHub Actions Docs](https://docs.github.com/en/actions)
