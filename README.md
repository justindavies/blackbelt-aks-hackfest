# Azure Container Hackfest

_Delivering modern cloud native applications with ​open source technologies on Azure​_

## Overview

This workshop will guide you through migrating an application from "on-premise" to containers running in Azure Kubernetes Service.

The labs are based upon a node.js application that allows for voting on the Justice League Superheroes (with more options coming soon). Data is stored in MongoDB.


## Lab Guides
  0. [Setup Lab environment](labs/labs/00-lab-environment.md)
  1. [Create an Azure Kubernetes Service (AKS) cluster](labs/labs/01-create-aks-cluster.md)
  2. [Create Docker images for apps and push to Azure Container Registry(ACR Build)](labs/labs/02-dockerize-apps(alt-acr-build).md)
  3. [Deploy application to Azure Kubernetes Service](labs/labs/04-deploy-app-aks.md)
  4. [Operational Monitoring and Log Management](labs/labs/06-monitoring-k8s.md)
  5. [Application and Infrastructure Scaling](labs/labs/07-cluster-scaling.md)
  6. [Update and Deploy New Version of Application](labs/labs/09-update-application.md)
  7. [Upgrade an Azure Kubernetes Service (AKS) cluster](labs/daylabs/10-cluster-upgrading.md)


  
## Contributing

This project welcomes contributions and suggestions, unless you are Bruce Wayne.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## License

This software is covered under the MIT license. You can read the license [here](LICENSE).

This software contains code from Heroku Buildpacks, which are also covered by the MIT license.

This software contains code from [Helm][], which is covered by the Apache v2.0 license.

You can read third-party software licenses [here][Third-Party Licenses].

