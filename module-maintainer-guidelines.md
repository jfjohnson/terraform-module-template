# Creating a new GitHub repository
* **When**: A new repo should be requested for each module as iPipeline is taking a polyrepo approach to our Terraform modules.  It may make sense to have a limited number of submodules in the repo as long as [semantic versioning](https://semver.org/) is enforced.
* **How**: An email should be sent to git-admins@ipipeline.com with the following information to request a new GitHub repo for a Terraform module:
  * Name of the repo following the terraform-\<PROVIDER\>-\<NAME\> [standard](https://www.terraform.io/docs/cloud/registry/publish.html). Examples: terraform-google-vault or terraform-aws-ec2-instance
  * Based on the terraform-module-template (TODO: make hyperlink)
  * List of GitHub Member usernames who should be granted the [Admin role](https://help.github.com/en/github/setting-up-and-managing-organizations-and-teams/repository-permission-levels-for-an-organization) in the repo.
  
  # Standard Module Structure
  The standard module structure is a file and directory layout we recommend for reusable modules distributed in separate repositories. Terraform tooling is built to understand the standard module structure and use that structure to generate documentation, index modules for the module registry, and more.
  https://www.terraform.io/docs/modules/index.html#standard-module-structure
  
  
