# Table of Contents
* [Creating a new GitHub repository](#creating-a-new-github-repository)
* [Customizing your newly provisioned GitHub repository](#customizing-your-newly-provisioned-github-repository)
* [Standard Module Structure](#standard-module-structure)
* [Contributing & Approving Changes](#contributing--approving-changes)
* [Creating a Release](#creating-a-release)
* [Roles & Permissions](#roles--permissions)


# Creating a new GitHub repository
## When to write a module 
* In principle any combination of resources and other constructs can be factored out into a module, but over-using modules can make your overall Terraform configuration harder to understand and maintain, so we recommend moderation.
* A good module should raise the level of abstraction by describing a new concept in your architecture that is constructed from resource types offered by providers.
* A new repo should be requested for each module as iPipeline is taking a polyrepo approach to our Terraform modules.  It may make sense to have a limited number of submodules in the repo as long as [semantic versioning](https://semver.org/) is enforced.
* It is not recommend writing modules that are just thin wrappers around single other resource types. If you have trouble finding a name for your module that isn't the same as the main resource type inside it, that may be a sign that your module is not creating any new abstraction and so the module is adding unnecessary complexity. Just use the resource type directly in the calling module instead.
## How to request a new GitHub repository for your module
* An email should be sent to git-admins@ipipeline.com with the following information to request a new GitHub repo for a Terraform module:
  * Name of the repo following the terraform-\<PROVIDER\>-\<NAME\> [standard](https://www.terraform.io/docs/cloud/registry/publish.html). Examples: terraform-google-vault or terraform-aws-ec2-instance
  * Based on the terraform-module-template (TODO: make hyperlink)
  * List of GitHub Member usernames who should be granted the [Admin role](https://help.github.com/en/github/setting-up-and-managing-organizations-and-teams/repository-permission-levels-for-an-organization) in the repo.
  

# Customizing your newly provisioned GitHub repository
* You should add a short description explaining the functionality of the Terraform module(s) in your repository to the repository description.
* (label your repo..aka Topics... @Wayne-Ennis ...CCOE-923)
* The .github/CODEOWNERS file in the template grants permissions to the code owners in the template repository. You should modify the [.github/CODEOWNERS](.github/CODEOWNERS) in your repository with your code owners.


# Standard Module Structure
The [standard module structure](https://www.terraform.io/docs/modules/index.html#standard-module-structure) is a file and directory layout we recommend for reusable modules distributed in separate repositories. Terraform tooling is built to understand the standard module structure and use that structure to generate documentation, index modules for the module registry, and more.

```
├── README.md
├── main.tf
├── outputs.tf
├── variables.tf
├── ...
├── modules/
│   ├── nestedA/
│   │   ├── README.md
│   │   ├── variables.tf
│   │   ├── main.tf
│   │   ├── outputs.tf
│   ├── nestedB/
│   ├── .../
├── examples/
│   ├── exampleA/
│   │   ├── main.tf
│   ├── exampleB/
│   ├── .../
```
  
# Contributing & Approving Changes
* All contributions should follow the guidelines explained in [CONTRIBUTING.md](CONTRIBUTING.md).

# Creating a Release
* 


# Roles & Permissions
### Contributors
These users are assigned the *Write* role in order to push to your project, although the master branch is protected from contributors.  The terraform-contributors team members will have *write* role to encourage contribution to the repository.
### Code Owners
These users are also assigned the *Write* role in order to push to your project, but they are also listed in the CODEOWNERS file in order to approve pull requests and push to the master branch.  There should be at least 2 code owners assigned per repository.
### Maintainers
Users assigned the *Admin* role will have full access to the project.  This role should be limited to a select few individuals. Organizational and Account admins would also have repository admin role priveleges if they were required so it may not be required for every repository to have admins explicitly assigned.

See [Repository permission levels for an organization](https://help.github.com/en/github/setting-up-and-managing-organizations-and-teams/repository-permission-levels-for-an-organization) for more detailed information on permission levels.

