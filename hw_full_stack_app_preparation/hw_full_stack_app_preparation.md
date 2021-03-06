# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using no frameworks, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
The request.js defines the routes for the games resource.

2. What are the the responsibilities of server.js?
The server.js is responsible for loading static files onto the browser and directing responses and requests using any router. In this case the gamesRouter. It also is the connection between the client and the database. It also parses the JSON.


3. What are the responsibilities of the `gamesRouter`?
The gamesRouter is responsible for providing the restful routes for any requests and responses then using these to communicate with the database.


4. What process does the the client (front-end) use to communicate with the server?
The client submits a form which posts a request to the CREATE route. It also receives responses/data via the index, show routes. These are both done using "Xmlhttprequests" although the information is actually sent in JSON and not XML.

5. Which of the games API routes does the front-end application consume (i.e. make requests to)?
Create and Delete

## Extensions

1. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

2. Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
ObjectId is a unique identifier and is used to identify objects so they can be deleted, updated etc.
