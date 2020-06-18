# Table of Contents
* [Why to fork a public module](#why-to-fork-a-public-module)
* [What to consider when forking a public module](#what-to-consider-when-forking-a-public-module)
* [How to fork a public module/repo](#XXXXX)
* [Contributing to forked modules](#XXXX)
* [Roles & Permissions](#roles--permissions)

# Why to fork a public module
* There are well established and widely used Terraform modules being maintained by the Terraform community that can be consumed in order to let iPipeline focus on building value in our Terraform code where we differentiate ourselves. (aka. "don't reinvent the wheel)

# What to consider when forking a public module
## HashiCorp Verified Modules
It is recommended to consume HashiCorp [Verified modules](https://www.terraform.io/docs/registry/modules/verified.html) when possible. Verified modules are actively maintained by contributors to stay up-to-date and compatible with both Terraform and their respective providers.  The blue verification badge appears next to modules that are verified.
### HashiCorp Official
* Official modules owned and maintained by HashiCorp.
### Partners
* Partner modules are owned and maintained by a technology company that has gone through the HashiCorp partner provider process and maintains a direct connection to HashiCorp.


### Licensing
* HashiCorp does not review the licensing the modules are published under. Please see the [licensing considerations](#licensing) below.

## Other Modules
### Trusted Author(s)
* Forking modules mitigates much of the risk consuming open source code as ultimately we are in control of the code we use, but it still advisable to fork repositories from reputable authors.
### Licensing
* James Johnson TBD
### Actively Maintained
* It is important to consume open source modules that are actively maintained by the community. Using the pulse insights in GitHub over the past month is a good view into the recent activity on a module
### Usage
* A module that is widely used, is more likely to have 
