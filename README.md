# Node, Restify, New Relic 
 
Welcome to the Node-Restify-New Relic demo! This guide will provide all the required development environment setup steps, files, and instructions to build a basic web application using Node and Restify. We will also monitor this application with the New Relic Node.js APM agent and try out some custom instrumentation features. 
 
### Part 0: Development Environment
In this project we will be using a few free or open source tools to build our application. To start with, you will need to install the [LTS version of Node](https://nodejs.org/en/download/). Throughout the tutorial videos, I will be using [Visual Studio Code](https://code.visualstudio.com/download) as my IDE, it is a free code editor from Microsoft with a very low learning curve. Finally, we will use [Postman](https://www.getpostman.com/apps) to make API calls and [DB Browser for SQLite](https://sqlitebrowser.org/) to view our database. Once you have all these installed, you should also pull down the starting files folder for the project. We will be coding most of this application together, but I have written a couple Node scripts to set up the database and configured the package.json with all the dependencies we will need for the project.
 
### Part 1: Back End Development
In this section we will connect to our SQLite database and build out our API endpoints in the app.js file of our application. *(For fun, our demo application is going to house the nerdiest New Relic NRQL jokes we can think of. Feel free to change this in your version of the project to make it your own!)* We will start with creating the GET, POST, and DELETE requests, and finish with adding some basic data validation. We then test this functionality using Postman to make calls to our API endpoints while running the application locally.
1. [Create app.js and GET endpoint](https://drive.google.com/open?id=1389MYypHJBBfUHVQlco-_xDW4cCdkpj4)
2. [Add POST and DELETE endpoints](https://drive.google.com/open?id=1YyRQgey6SIbxWcf82DhMr5514QCuJtRr)
3. [Add data validation](https://drive.google.com/open?id=135n2JR_Hb5EdMCj1Wv2agKyeW9BTOAXd)
 
### Part 2: Front End Development
In this section we build out the HTML framework for the front end of our application, along with the JavaScript to connect to our back-end. We adjust our code as we go to make sure the page pulls information from the database in a manner that will make sense to our end user. In the end, users can view, add, and delete jokes through the front end of our application.
1. [Create index.html template and add static route](https://drive.google.com/open?id=1vIThYJsWIj-mc1z0syEnEidrGB9S6tgZ)
2. [AJAX - Get all data](https://drive.google.com/open?id=1dxGbgw3he-L1rnt7zs4jusdqqWh5LeUT)
3. [AJAX - Post new data](https://drive.google.com/open?id=1BhNrtM38KfLne66hwT4mlUCShV2A5lA6)
4. [AJAX - Delete data](https://drive.google.com/open?id=1wwR8v2eVclteRvz2O8B4cdkSy54QB1xe)
 
### Part 3: New Relic
Now that we have the front and back end pieces of our application working, we are going to install and configure the New Relic Node.js APM agent. You will need to make sure you have created a [New Relic account](https://newrelic.com/signup) and can locate your New Relic [license key](https://docs.newrelic.com/docs/accounts/install-new-relic/account-setup/license-key#finding) before working through this portion of the project. We will compare the out-of-the-box instrumentation with some custom instrumentation options configurable within the agent and our application.
1. [Install the New Relic Node.js Agent](https://drive.google.com/open?id=1zPyFZBiWhBGC5HGKpqOduhpXI6YHnr0y)
2. [Send 403’s and record custom attributes](https://drive.google.com/open?id=1fxWjIQaxhBTgfb_ps-sjG1Br9rdwQzw7)
3. [Set transaction names](https://drive.google.com/open?id=1wdhIEvH7372vrRnG3tPgUXmI20jbNMWK)
4. [Create custom transactions](https://drive.google.com/open?id=1ircrWQVb1IvfxH-KXL5LXmnMERAptR0a)
5. [Ignore specific error status codes](https://drive.google.com/open?id=1A0s4Pv6nHTKFICj5IpJ8UNeez3I1AMfZ)
6. [Use the notice error API](https://drive.google.com/open?id=1U-inZ5rSKu7XmDKzRPfkJNvDtvh7ygCB)
7. [Move the require statement](https://drive.google.com/open?id=1DKZTLk5E7qG3Tko2lNxgZZaFkuTEl_xg)
8. [Record custom metrics](https://drive.google.com/open?id=1XSa53PgwwGhpXi7ua27aZH3iGcDoANx5)
 
### Part 4: Deploy
If you want to run this application in the wild, I recommend deploying to Heroku. Creating a [free account](https://signup.heroku.com/) and deploying using the CLI is easy, and step by step commands are provided. Bonus: if you’ve followed the steps to install and configure the New Relic Node.js agent before deploying the application, you can use New Relic Synthetics to ping your live Heroku application and generate monitoring data to view in the New Relic UI!
