# Terraform Questions

### What is the purpose of state file in Terraform?
### How does the states maintained in Terraform?

Ans.

### Where does .tfstate file created? and who creates it?

Ans.

### How do you manage Terraform using Azure DevOps?

Ans. 

### What is Terraform import and how does it work?

Ans.

### What is taint and untaint in Terraform? Explain with example!

Ans. The ```terraform taint``` command informs Terraform that a particular object has become degraded or damaged.

**This command is deprecated, because there are better alternatives available in Terraform v0.15.2 and later.**

If your intent is to force replacement of a particular object even though there are no configuration changes that would require it, we recommend instead to use the ```-replace``` option with ```terraform apply```. 

**Example:**
```terraform apply -replace="aws_instance.example[0]"```

source: 
https://www.terraform.io/docs/cli/commands/taint.html

https://www.terraform.io/docs/cli/state/taint.html

### How to test the terraform scripts?

Ans. Use the ```terraform validate``` command but use the ```terraform plan``` command instead, which includes an implied validation check.


