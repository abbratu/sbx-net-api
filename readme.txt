dotnet new sln

dotnet new gitignore

dotnet new webapi -o SbxNetApi
dotnet sln add ./SbxNetApi


cd SbxNetApi
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.InMemory