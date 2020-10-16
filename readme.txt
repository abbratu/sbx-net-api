dotnet new sln

dotnet new gitignore

dotnet new webapi -o SbxNetApi
dotnet sln add ./SbxNetApi


cd SbxNetApi
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.InMemory


cd SbxNetApi
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design
dotnet add package Microsoft.EntityFrameworkCore.Design
dotnet tool install --global dotnet-aspnet-codegenerator
dotnet tool update -g Dotnet-aspnet-codegenerator
dotnet aspnet-codegenerator controller -name UsersController -async -api -m User -dc ApiDbContext -outDir Controllers

cd SbxNetApi
dotnet add package Microsoft.AspNetCore.Mvc.Versioning