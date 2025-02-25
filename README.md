# Secure From Scratch - Angular / .NET Workshop
This repository contains a re-work of the secure coding lab provided by the team as [Secure From Scratch](https://github.com/SecureFromScratch/Workshops). The lab has been scaled down and re-worked to be accessible by a student audience. This workshop is designed to help you learn and practice secure coding practices.

## Getting to know the lab project
This project is a simulated recipe application
1. The front-end recipes-app has been written in Angular 17
2. The back-end recipes-api has been written in .NET 8.0 Core
3. The application is designed to work with a local instance of SQL Server
4. The extras folder contains text and an image for the recipes application
5. This repo includes a C# console application named AttackerConsole that can be used to run simulated attacks on the application

## Preparing for the workshop
If you wish to follow along during the workshop, you will need to have the application set up on your computer and running. To do so, follow these steps.
1. Clone this repo and download the contents so you have the files
2. Open the Angular project in VSCode
     1. If you do not already have Angular installed you can follow the steps [here](https://code.visualstudio.com/docs/nodejs/angular-tutorial) to get started. If you do not have the node packages installed you can use npm install from VS Code to load the packages for the application.
3. Open the .NET Core solution in Visual Studio 2022
4. Download SQL Server  - Express is sufficient [SQL Downloads](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
5. Download SQL Server Management Studio so you can create/manage databases on your server [SSMS](https://learn.microsoft.com/en-us/ssms/download-sql-server-management-studio-ssms)
     1. Find the recipes.mdf file that contains the database for this application under the recipes-api/data folder. Move it to the DATA folder for your installation of SQL Server
     2. In SSMS, attach the MDF file so the database is available in your server. Make sure it is named recipes.
     3. Review the appsettings.json file in the .NET application. Ensure the DefaultConnection string has the correct data source for your SQL Server. 
6. In the appsettings.json file, update the value for MyDeviceIP to be your private iPv4 IP address (not your public IP!)

### Running / Testing the Application
Once you have completed the above steps you can make sure your application is prepared for the workshop by doing the following:
1. Execute the Web API. Use the Swagger interface to test the Get Recipes endpoint and check you get a successful response
2. Execute the Angular App found in the recipes-app/src folder
3. Check the app can access the API. The Carrot Cake recipe should show on the main page.
     1. Get all the recipes va the Angular App
     2. Add a recipe via the Angular App. Check it shows on the page AND in Swagger
