# 1. Introduction
This project is one of two components in a microservices system built with .NET. 
Specifically, this module processes item data. The other module is responsible for storing inventory data and interacts with the item module via a message broker.

## [Knowledge Summary](/NOTE.md)


# 2. Technologies:
* Built on the .NET 5 platform
* Data storage in MongoDB
* Asynchronous communication via RabbitMQ message broker
* Reusable modules implemented with class libraries
* Deployment using Docker

# 3. Setup guide
## Config env
### Create global.json file
```text
{
    "sdk": {
        "version": "5.0.408"
    }
}
```
### Dowload package
```powershell
dotnet add package MongoDb.Driver
```

### Setting docker image
```powershell
docker run -d --rm --name mongoDbContainer -p 27017:27017 -v mongoDbData:/data/db mongo
```
### Using repository package instead
```powershell
dotnet add package Play.Common
```

### Add reference to Play.Catalog.Contracts
```powershell
dotnet add reference ..\Play.Catalog.Contracts\
```

### Add nuget packate to enable async cummunication by using publishing message via MassTransit
```powershell
dotnet add package MassTransit.AspNetCore
dotnet add package MassTransit.RabbitMQ
```
# 4. Ref
Project follows the guidelines provided by Julio Casal.