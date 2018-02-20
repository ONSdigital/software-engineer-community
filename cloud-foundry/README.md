# Cloud Foundry

> Please note. This guide is a curated list of information tailored to use of Cloud Foundry (hereon referred to as `cf`) within ONS. It does not attempt to replicate information already available via the internet or reinvent wheels.

- [Concepts](#concepts)
- [Cloud foundry cli tool](#cloud-foundry-command-line-tool)
- [Deploying apps](#deploying-apps)
- [See also](#see-also)


## Concepts

General `cf` concepts and primers on the architecture if you're interested can be found in the [official docs](https://docs.cloudfoundry.org/concepts/)

Highlights:

- [Cloud foundry overview](https://docs.cloudfoundry.org/concepts/overview.html)
- [Orgs, spaces, roles and permissions](https://docs.cloudfoundry.org/concepts/roles.html)


## Cloud Foundry command line tool

Most of your interaction with `cf` outside of a ci pipeline will be more than likely using the `cf cli` tool. Again, the [official cli docs](https://docs.cloudfoundry.org/cf-cli/) are a good place to start.

Highlights:

- [Getting started with the cli](https://docs.cloudfoundry.org/cf-cli/getting-started.html)
- [Full official cf cli refence](http://cli.cloudfoundry.org/en-US/cf/)


## Deploying apps

A good overview of the concepts and basic practice of deploying apps is covered in the [official docs under 'deploying and managing applications'](https://docs.cloudfoundry.org/devguide/deploy-apps/)

Highlights:

- [Considerations for designing and running apps](https://docs.cloudfoundry.org/devguide/deploy-apps/prepare-to-deploy.html)
- [Deploy an application](https://docs.cloudfoundry.org/devguide/deploy-apps/deploy-app.html)
- [Starting, restarting and restaging](https://docs.cloudfoundry.org/devguide/deploy-apps/start-restart-restage.html)
- [Application manifests](https://docs.cloudfoundry.org/devguide/deploy-apps/manifest.html)


## See Also

- [GDS Goverment PaaS 12 Factor and developing](https://docs.cloud.service.gov.uk/#12-factor-application-principles) - a good summary of the [12 factor](https://12factor.net) and how they related to a `cf` based environment as well as a general write up of `cf` concepts and principals. It's worth noting that not everything applies to our current environments (e.g. some backing services aren't available and we don't have paid plans etc)
- [Software Engineering Community standards](../standards/README.md) - usual SE Community standards apply to code created for `cf` deployments.