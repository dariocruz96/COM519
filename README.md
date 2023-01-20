# COM519
Avanced Database Systems (COM519) - Assessment 1: Proof of concept data-driven full stack web-application

Link to github repository: https://https://github.com/dariocruz96/COM519/<br>
Hosted on Cyclic: https://animal-crossing-fish.cyclic.app/<br>
Contributer: <strong>Dario Cruz</strong>

# How to Setup the Project 
- Download the zip file of the project.
- Unzip it wherever you want.
- Open the folder using Visual Studio Code.
- Open new terminal.
- Run 
```
npm install
```
- After that run 
```
npm run dev
```
- In the terminal you will see Example app listening at: The URL of the application. Press ctrl and click on the URl to start the application.
# Introduction
For this project it was required to create, test, and deploy, a proof of concept data-driven full stack web-application so I wanted to do something that would make sense for me.

I decided to go with a game that is played around the globe and that includes me, Animal Crossing New Horizons for Nintendo Switch.
Animal Crossing has around 240 000 players online daily and has sold around 40 million dollars since its release making it one of the most successful games for the console.

While playing the game, there is always something that bothering me, <strong>fishing</strong>! I never know if the fish I just got is worth the space in the inventory or if I can just throw it out and keep the good ones (£££) to sell later and the only way to find out is going to the store and try to sell them, but even then, I would have to sell them individually to know their exact price.

In the end of the day the same problems remained:
-	I can’t know the price while fishing
-	I have to go to the store and them sell individually to see the price
-	I can’t remember the price later
-	I make low money due to carrying worthless fish

<strong>*There must be a better way!*</strong>

  Using the animal crossing new horizons’ s dataset from Kaggle.com I created a web-app that allows players to check fish prices while they are fishing so they know if it is worth to keep them.



# System Overview

I used mongodb atlas to help me with my non-relational database and fish collection (Kaggle dataset) for data.

This web application structure is based on Model, Views and Controllers (MVC structure), where the user will interact with views (web pages), the view pages will send requests to controllers,  the controllers will write in the models and the models will store data in our database (MongoDB), going the other way around, database will retrieve data to the models, the controllers will read from the models sending a response to views, which will be visible to the user.

<strong>Diagram</strong><br>
![Diagram](/public/images/diagram.png)<br>


<strong> Home page </strong><br>
Simple home page with header menu connections to home, fish and create a new fish pages, three images and a footer with some hyperlinks.
![Home](/public/images/Home.png)<br>

<strong>Fish page</strong><br>
Page showing a list of fishes details such as name, selling price, spawn rate	and shadow size, have a create, edit and delete fish buttons. 
![fish](/public/images/fish.png)<br>

<strong>Create fish page</strong><br>
Page with inputs to create a new fish and add it to database.
![create-fish](/public/images/create-fish.png)<br>

<strong>Edit fish page</strong><br>
Page with inputs to change a fish details, showing the existing details.
![edit-fish](/public/images/edit-fish.png)<br>

# Key Design Decisions

I decided to go with a really simple, user-friendly design, not a lot of options or links, not a lot of images, simple to use and no explanation need at all.


# Database Design

I used a single collection because it provided me with all the information I needed and even "ignored" a few properties which I didn't find it important to be seen.
Mongoose prived a unique ID for each record and so it became very simple to interact with the database.
![database](/public/images/database.png)<br>


# Security and Scalability

I didn't provide any security to the web app which is something that can be done if this would be taken forward to a full project or a complete market ready app by creating user authentication and restrict access to some features.
Going forward with this proof of concept web application could be creating a full Animal Crossing help tool, using all the collections and properties provided in the Kaggle dataset and provide help with any aspect of the game to players. 
Doing a better styling would improve the web app a lot as well.

# Conclusion and reflection

Deploying this project in Cyclic makes it accessible to everyone and MongoDB/Mongoose allowed me to easly work with database, which following the MVC structure made it really simple and straight forward to create the web application.
Working with Git allowed to to go back in work a few times to confirmed to work versions and even work from different PCs and places.
While creating the first funcionalities gave a bit of work, the more there was to do the simpler it became, getting used to the structure flow and having some code as base made it possible to quickly add features and funcionalities.
