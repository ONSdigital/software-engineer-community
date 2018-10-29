
Use of GitHub at ONS
--------------------
Aligning with the GDS practice of "Coding In The Open" means that a lot of public repositories end up on our GitHub organisation.

This document defines the agree standards and policies for using GitHub at ONS.

## Responsibility for GitHub Usage at ONS

### Overall Responsibility
The Head of Technology Development assumes responsibility for the policies on using GitHub at ONS.

Ultimately the Head of Technology has the final say on how teams with Digital Services & Technology (DST) at ONS utilise GitHub but will take advice from the Technical Leads Community of Practice. The caveat is Digital Publishing as they don't fall under the DST umbrella and tehrefore could not be mandated to work in a partricualr way. As such DP will have input into and will aim to comply to theese standards but they cannot be manadted by DST.

#### Operational Responsibility
Day-to-day responsibility for managing the use of GitHub and defining and governing its use lies with the Technical Leads.

The Technical Lead Community of Practice will nominate one of its members to represent them but decisions will be made via community consensus.

If the community cannot agree then the Head of Technology Development has the casting vote on any decision.

Information Assurance
The Information Assurance Community of Practice will nominate one of its members to risk assess the use of GitHub at ONS and approve this policy.

#### Named Representatives

| Name | Role |
| Julie Caldwell| Head of Technology Development (DST)|
| Ian Kent | Digital Publishing |


# Policies
### All code should reside under the ONSDigital organisation
All code repositories in GitHub should be created under the umbrella of the ONSDigital organisation.

The administrators of the organisation are the Technical Leads.

The Technical Leads will grant and revoke membership of the organisation.

### Membership of the ONSDigital organisation must be actively managed
All Tech Leads are Administrators of ONSDigital
Managing teams within the ONS GitHub organisation
Teams should be created aligning with the product teams at ONS.

Each Technical Lead is responsible for managing her or her team(s).

#### Managing movers/leavers/joiners
If an individual leaves ONS then the Technical Lead should also remove them from the ONSDigital organisation.

GitHub audits joiners and leavers

### GitHub accounts must be traceable to an individual
All accounts should be easily identifiable to their owners.

GitHub Profile
It is mandated that individuals should populate their GitHub account profile with their real forename and surname.

The GitHub username must not be offensive or anything deemed inappropriate by the Technical Lead of the individual.

Personal Accounts
It is acceptable for an individual to use their own GitHub account or an ONS dedicated GitHub account according to their personal preference.

However only one account per individual should be registered to the ONSDigital organisation.

### Any member of the ONSDigital organisation can create a repository
Anyone in the organisation can create a repository.

### For service repositories the master branch should be protected.

### Administrators of the ONSDigital organisation must have two-factor authentication enabled
A condition of being granted administration right on the organization is to have two-factor authentication enabled.

As they are administrators all Technical Leads must have two-factor authentication enabled on their accounts.

Organisation Members
It is strongly encouraged that all users have two-factor authentication enabled on their accounts. Reasonable reasons for not having it enabled are required.

Service Accounts
Service accounts used by continuous integration solutions do not require two-factor authentication.

Service accounts should have the minimal permissions required to complete the required task.

### Signed commits are encouraged
GitHub supports signed commits so other people can verify that your work comes from a trusted source. If a commit or tag has a GPG or S/MIME signature that is cryptographically verifiable, GitHub marks the commit or tag as verified.

Digital publishing validate the GPG key used against a list of known keys (managed in a github repo) and refuse to build either unsigned commits or commits signed by a key we don't recognise.

At this stage signed commits are not mandated across ONS.

### Webhooks from GitHub to on-network build systems must be via the CA API Gateway
Webhooks are used to trigger builds on continuous integration tools such as Jenkins, Concourse or Travis CI.

Triggering off-network builds in the cloud from GiHub is authorised as per standard connectivity.

Triggering on-network builds from GitHub is authorised only via the CA API Gateway.

All repositories from the ONSDigital organisation should be whitelisted.

### Non-ONS contributors to ONS repositories are not currently supported
Currently we do not support changes from outside of members of the ONDigital GitHub organisation.

If we get an unsolicited pull request from outside of the organisation it must not be merged.

If we are to allow outside contributors a policy for accepting changes will need to be developed and agreed.

### Assume everything is public
Encrypt anything that may be sensitive

Be mindful of comments and variable names

Commit messages should be well formed and not offensive or overly critical

Write good pull requests

Remember that the repositories are a public face of ONS

Ensure test data is anonymised
Test data shouldn't relate to real companies or individuals





