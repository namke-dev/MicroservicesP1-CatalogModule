# DotNetMicroservicesWrapUp

Create global.json file
```text
{
    "sdk": {
        "version": "5.0.408"
    }
}
```
Dowload package
```powershell
dotnet add package MongoDb.Driver
```

Setting docker image
```powershell
docker run -d --rm --name mongoDbContainer -p 27017:27017 -v mongoDbData:/data/db mongo
```
Using repository package instead
```powershell
dotnet add package Play.Common
```

this project follow instruction of Mr. Julio Casal

source: https://www.youtube.com/watch?v=ByYyk8eMG6c