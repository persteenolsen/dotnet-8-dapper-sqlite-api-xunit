# dotnet-8-dapper-sqlite-crud-api-xunit

.NET + VS Code + xUnit - Setup Unit Testing and Code Coverage in ASP.NET Core

# Last updated

- 11-11-2024

# Source code
dotnet-8-dapper-sqlite-crud-api

# .NET Version
.NET 8

# DB
SQLite

# ORM
Dapper

# NuGet Packages with commands
- dotnet add package AutoFixture
- dotnet add package Moq
- dotnet add package coverlet.msbuild

# VS Code Extensions

- NET Core Test Explorer
- Coverage Gutters

# Unit Tests
xUnit

# Coverage Reports

dotnet tool install -g dotnet-reportgenerator-globaltool

# Run tests and view the code coverage by VS Code

- Run the Tests by open the .NET Test Explorer ( click the Testing tab in the left side of VS Code)

- After the Tests pass there should be a generated code coverage file at /WebAPI.Tests/TestResults/
lcov.info. The file contains coverage data and is not meant to be directly human readable

- Now open the WebAPI/Services/UserService.cs class and enable Coverage Gutters by clicking Watch in the VS Code status bar. The gutter next to the line numbers should be green for covered lines and red for uncovered lines, and the status bar should show the percentage that the file is covered

- By clicking in the WebAPI/Services/UserService.cs should show 42 % covered at the bottom of VS Code

- Try click in the WebAPI/Entities/User.csfile which should show 100 % covered

- Note: Also make sure to create or update the /.vscode/tasks.json file to generate an HTML coverage report based on the lcov.info file

- Run the task by selecting: Terminal > Run Task... > generate coverage report

That is a setup to run unit tests and generate code coverage reports quickly and easily with VS Code for ASP.NET Core projects :-)


# Run tests outside VS Code

- First make sure to Right Click the folder WebAPI.Tests by Powershell or Promt and type dotnet restore

- Then Right Click the folder WebAPI.Tests by Powershell or Promt and type dotnet test

- The results of the Tests will be displayed 







