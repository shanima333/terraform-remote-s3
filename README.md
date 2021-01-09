### Terraform Remote State S3 | Terraform Remote State | Terraform State File

We can store the terraform state file as a  key in a bucket on Amazon S3. For that we need to add below code to the terraform file

terraform {
  backend "s3" {
    bucket = "shaniterraform"
   key    = "myproject/dev/terraform.tfstate"
   region = "us-east-2"
   access_key = ""
  secret_key = ""
  }
}

Provide secret_key and access_keys 

Then run 

terraform init
