[![Board Status](https://dev.azure.com/sachin77/2fdf9053-31ca-49c0-90e9-60566565a48b/6c069560-bddf-4d4d-93b1-acc06bdebd0b/_apis/work/boardbadge/1e74de87-744f-4316-bb83-fee7b78b7c86)](https://dev.azure.com/sachin77/2fdf9053-31ca-49c0-90e9-60566565a48b/_boards/board/t/6c069560-bddf-4d4d-93b1-acc06bdebd0b/Microsoft.RequirementCategory)
# SmartHotel360
During **Connect(); 2017** event this year we presented beautiful app demos using Xamarin and many features of Azure. For //build/ 2018's keynote, we updated some components of the back-end API code to support **Azure Kubernetes Service (AKS)**.

# SmartHotel360 Repos
For this reference app scenario, we built several consumer and line-of-business apps and an Azure backend. You can find all SmartHotel360 repos in the following locations:

- [SmartHotel360](https://github.com/Microsoft/SmartHotel360)
- [IoT](https://github.com/Microsoft/SmartHotel360-IoT)
- [Mixed Reality](https://github.com/Microsoft/SmartHotel360-MixedReality)
- [Backend](https://github.com/Microsoft/SmartHotel360-Backend)
- [Website](https://github.com/Microsoft/SmartHotel360-Website)
- [Mobile](https://github.com/Microsoft/SmartHotel360-Mobile)
- [Sentiment Analysis](https://github.com/Microsoft/SmartHotel360-SentimentAnalysis)
- [Registration](https://github.com/Microsoft/SmartHotel360-Registration)

# SmartHotel360 - Backend Services

Welcome to the SmartHotel360 AKS repository. Here you'll find everything you need to run the backend services locally and/or deploy them in a AKS cluster.

## Getting Started

SmartHotel360 uses a **microservice oriented** architecture implemented using containers. There are various services developed in different technologies: .NET Core 2, Java, and Node.js. These services use different data stores like PostgreSQL and SQL Server. 


We have added an ARM template so you can automate the creation of the resources

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3a%2f%2fraw.githubusercontent.com%2fMicrosoft%2fSmartHotel360-Backend%2fmaster%2fSource%2farm%2fsmarthote360.backend.deployment.json"><img src="/Documents/Images/deploy-to-azure.png" alt="Deploy to Azure"/></a>

1. [Demo Setup](Documents/Setup.md) - Create the Azure resources and demo environment setup, and deploy the SmartHotel360 services to the AKS Cluster.

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
