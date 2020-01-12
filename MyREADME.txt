# Research for .NET Core to Oracle DB connect
- Tutorial for 'ContosoUniversity' app
{
    @: https://docs.microsoft.com/en-us/aspnet/core/data/ef-rp/intro?view=aspnetcore-2.1&tabs=visual-studio-code
    - Repo with sample code:
     --> https://github.com/aspnet/AspNetCore.Docs/tree/master/aspnetcore/data/ef-rp/intro/samples
}
- Last: https://docs.microsoft.com/en-us/aspnet/core/data/ef-rp/intro?view=aspnetcore-2.2&tabs=visual-studio-code#examine-the-context-registered-with-dependency-injection

NOTES:
- The 'ContosoUniversity' app outside was done unintentionally upon first create using CLI commands.
 It will get used for test purposes.
 - When pointing to specific framework: 1) instal if needed framework:
  dotnet new --install "Microsoft.DotNet.Web.ProjectTemplates.2.1"
  2) execute with framework CLI option: dotnet new mvc --framework netcoreapp2.2
-- NuGet actually automatically looks up the framework online at CLI execution if not installed
 --> https://github.com/dotnet/docs/issues/14572#issuecomment-534586037
--- The file '*.csproj' for each project contains '<TargetFramework>netcoreapp2.1</TargetFramework>'
- Scaffolding through CLI. scaffolding tool produces pages for Create, Read, Update, and Delete (CRUD) operations
 for model classes:
{
  dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design --version 2.1.0
  dotnet tool install --global dotnet-aspnet-codegenerator [--version 2.1.0]
  dotnet aspnet-codegenerator razorpage -m Student -dc ContosoUniversity.Models.SchoolContext -udl -outDir Pages/Students --referenceScriptLibraries
}