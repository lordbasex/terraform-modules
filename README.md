# terraform-modules


# Module Backend S3

## main.tf
```
module "backend" {
  source       = "github.com/lordbasex/terraform-modules/aws/backend"
  aws_region   = var.aws_region
  project_name = var.project_name
}
```

## provider.tf
```
provider "aws" {
  region = var.aws_region
}
```

## variables.tf
```
variable "project_name" {
  description = "Everything for state related terraform"
  type        = string
  default     = ""
}

variable "aws_region" {
  description = "AWS region"
  type        = string
  default     = ""
}
```

## terraform.tfvars 
```
project_name = "MyProjectName"
aws_region   = "us-east-1"
```
