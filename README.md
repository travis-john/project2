# Project 2

## Movie Browser - Everything Movies 

Our project is an application that shows you movies.  You can filter the movies shown by several different criteria: 

* popular
* now playing 
* upcoming 
* top-rated  (based on user ratings)
* search keywords 

Users can login and then save watch lists, including deleting movies from their watch list.  

Target audience:  anyone! 

## Application Requirements

Our application meets the project requirements: 

* Must use a Node and Express server
* Used NPM packages - Express, Mysql, sequelize, passport, eslint, lodash
* Must be backed by a MySQL database and an ORM (we used Sequelize)
* Must utilize both GET and POST routes for retrieving and adding new data
* Must be deployed using Heroku (with data)
* Must utilize at least one new third-party API - we used The Movie Data Base https://www.themoviedb.org/
* Must have a polished UI
* Must use a CSS framework _other than_ Bootstrap - we used Materialize 
* Must follow MVC paradigm
* Must meet good quality coding standards (indentation, scoping, naming)
* Must use Handlebars.js


## Presentation  

Our presentation can be found here (https://docs.google.com/presentation/d/1rp-eut0BSmu0XBw5rpXWZnLlzF5B4szaab8FGgtGVBY/edit?usp=sharing) 

Heroku Deployment - https://whispering-dawn-54949.herokuapp.com/

 
## Internals 

The application uses Sequelize to create two tables in the watchList_db: 
 
* Users - has columns id, email, and encrypted password 
* Movies - has columns id, movie (the key used in the movie database API), and a foreign key of the user who saved that  movie to their watchlist 

## Routes 

* /, /popular - the list of most popular movies
* /playing - what's now playing 
* /upcoming - movies being released soon 
* /toprated - based on user ratings 
* /watchlist - shows watchlist (only displayed on menu bar when user is logged in)

* /api/login - takes returning user to login
* /api/signup - new user signup 
* /api/signout - current user signout 
* /api/:id - returns the details for that movie id 
* /api/search/:searchstring
* /api/addwatchlist - adds the movie to the watchlist of the user that is logged in, if not logged in sent to login screen 
* /api/deletewatchlist/:movieid - deletes the movie from the watchlist of the current user 

## Handlebar files 

* index.handlebars is used to display all lists except search results
* search.handlebar is used to display search results 
* info.handlebar is used to display a single movie   
* navbar.handlebar is used to create the navigation bar  

## Partials handlebar files  

* card.handlebar is used to display a single movie as a materialize "card" on the index and search pages 
* movie-info.handlebar is used to display the movie information on the info.handlebar page 

## Potential enhancements 

* Let users screen the movies they select by genres
* Display more than the first page of results 
* Where a movie is playing near you 
* Parental controls 
