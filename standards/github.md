
# GitHub usage policy at ONS (Draft status) 

This document defines the agreed GitHub standards in line with ONS Source Control policy (add a link).

## Responsibility for GitHub Usage at ONS

### Overall Responsibility

The Head of Software Engineering Practice assumes responsibility for the policies on using GitHub at ONS.

Ultimately the Head of Software Engineering Practice has the final say on how teams with Digital Services & Technology (DST) at ONS utilise GitHub but will take advice from the **Technical Advisory Group or Technical Lead**s _Community of practice_. 

### Operational Responsibility

- Day-to-day responsibility for managing the use of GitHub and defining and governing its use lies with the **Technical Lead or nominated Sr. team member**s.

- The **Technical Lead** _Community of practice_ will nominate atleast one of its members to represent them but any decisions to update this document will be made via community consensus (through Technical Advisory Group)

- The **Security Division** will nominate one of its members to risk assess the use of GitHub at ONS and approve this guidance/standards.

### Named Representatives

- **TBD** - Technical Advisory Group 
---

## Policies

- [Code Repositories](#code-repositories)
- [Organisation Membership](#organisation-membership)
  - [Managing movers/leavers/joiners](#managing-moversleaversjoiners)
- [Github Accounts](#github-accounts)
- [Signed Commits](#signed-commits)
- [Webhooks into ONS](#webhooks-into-ons)
- [Assume everything is public](#assume-everything-is-public)
- [External contributors](#external-contributors)

### Code Repositories

All ONS code repositories in GitHub should be created under the approved ONS gitHub organisations (see Source Control Policy (Add a link link).  By default ONSdigital organisation should be used for all new repositories).

- **Administration** - the administrators of the organisation are the **Technical Lead or nominated Sr. team member**s.

- **Repository creation** - anyone in the ONSdigital organisation can create a repository.

- **Protection** - for service repositories the master branch should be protected.

### Organisation Membership

Membership of the ONSdigital organisation is administered and actively managed by the **Technical Lead or nominated Sr. team member**s

- **Administrators** - all **Technical Lead or nominated Sr. team member**s are administrators of ONSdigital.

- **Team management** - each **Technical Lead or nominated Sr. team member**s is responsible for managing their team(s).

- **Team organisation** - teams should be created aligning with the product teams at ONS.

#### Managing movers/leavers/joiners

- For a new joiner to the gitHub ONSdigital organisation, the **Technical Lead or nominated Sr. team member**s should raise a [ServiceNow ticket](https://ons.service-now.com/sp?id=sc_cat_item&sys_id=f0b3c9a41b271150b51ea6c7b04bcb8e)
- If an individual leaves ONS then the **Technical Lead or nominated Sr. team member**s should also remove them from the ONSdigital organisation.

- **Audit** - GitHub audits joiners and leavers via the audit log.

### GitHub accounts

- **GitHub Profile** - all individuals should populate their GitHub account profile with their real forename and surname.

- **Username** - must not be offensive or anything deemed inappropriate by the **Technical Lead or nominated Sr. team member**/ .

- **Personal Accounts** - it is acceptable for an individual to use their own GitHub account or an ONS dedicated GitHub account according to their personal preference. However only one personal account per individual should be registered to the ONSdigital organisation. However, where personal account is used the user should add ONS official email address as secondary email on the GitHub profile.

### Repository settings

#### Visibility

Repositories should be created a _public_ by default unless you have a specific need for them to be _internal_ or _private_, this is in line with [UK Govt guidline - Be open and use open source] (https://www.gov.uk/guidance/be-open-and-use-open-source). For more information please see [Assume everything is public](#assume-everything-is-public)). 

In case it is agreed that specific repository cannot be public, the readme section of that specific respository should clearly provide reasoning for that and the information about approving authority.

  
#### Collaborators

Only teams should be granted access to repositories. This makes it clear why the access is needed and helps to ensure people have correct permissions within team moves.

If there is an explicit need for an individual to be granted access this should be agreed with **Technical Lead or nominated Sr. team member.**

**(Note for Fahad)** - How the outside collabrator is given the access)??

#### Signed commits

GitHub supports signed commits so other people can verify that your work comes from a trusted source. If a commit or tag has a GPG or S/MIME signature that is cryptographically verifiable, GitHub marks the commit or tag as verified.

Digital publishing validate the GPG key used against a list of known keys (managed in a github repo) and refuse to build either unsigned commits or commits signed by a key we don't recognise.

- Signed commits are encouraged but not mandated

### Webhooks into ONS

Webhooks from GitHub to on-network build systems must be via the CA API Gateway 
  
- Webhooks are used to trigger builds on continuous integration tools such as Jenkins, Concourse or Travis CI.

- Triggering off-network builds in the cloud from GiHub is authorised as per standard connectivity.

- Triggering on-network builds from GitHub is authorised only via the CA API Gateway.

- All repositories from the ONSdigital organisation should be whitelisted.

### External contributors

Currently we do not support changes from outside of members of the ONSdigital GitHub organisation.
  
- **Unsolicited pull requests** - if we get an unsolicited pull request from outside of the organisation it must not be merged. It should be raised to the **Technical Lead** _Community of practice_.

- **The future** - we may choose to allow external contributors at a later date, but a policy for accepting changes will need to be developed and agreed.


### Assume everything is public

It should always be assumed that anything published to Github _is_ or _will be_ public and should be treated as such.

- **Private is not secret** - private repositories may be used, but you **must not** use them to enforce security by obscurity (see _encryption_ and _anonymisation_). Always assume they may be exposed (intentionally or otherwise) or made public in the future.

- **Limit exposure - encryption** - encrypt anything that may be sensitive (configuration / test data etc)

- **Limit exposure - anonymisation** - never publish real or apparently real data (test data etc shouldn't relate to real companies or individuals)

- **Public perception** - the ONSdigital organsiation is a public face of ONS. Be mindful of comments, pull requests, variable names etc (nothing offensive and never assume implicit knowledge)

- **Commit messages and pull requests** - should be well formed and always descriptive. Do not simply put links to / code numbers of stories in internal tracking systems that are unavailable to others.
