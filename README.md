# anything-but-a-pantry-manager

# Kahu 2018 Final Project

I often come home and have no energy to be creative enough to think of what to cook, I wish there was an app that could give me ideas and plan out meals around some of the food that needs to be eaten!


## User Stories

### MVP

As a user:
* I want to recieve a recipe based on 1 ingredient
* I want to recieve a recipe that knows my dietary and personal food preference
* I want to log in and have a profile

### Stretch 1
* I want to receive a recipe based on more than one ingredient
* I want to be able to tick thing off a recipe list to get an accurate shopping list
* I want to be able to plan X amounts of meals for one shopping list
  
### Stretch 2
* I want to reject a recipe and get a new one
* I want to give raitings to my recipes
* I want to share with my friends

  ---

## Views (Client Side)
  | name | purpose |
  | --- | --- |
  | App |  |
  | Login |  |
  | Register |  |
  | Profile |  |
  | GenerateRecipe |  |
  | Recipe |  |


## Reducers (Client Side)

  | name | purpose |
  | --- | --- |
  |  |  |
  |  |  |
  |  |  |
  |  |  |
  
 ## Actions
 
 ### meetings
 
 | type | data | purpose | 
 | --- | --- | --- | 

 ### users 
 | type | data | purpose |
 | --- | --- | --- |
 
 ### currentMeeting 
  | type | data | purpose | 
| --- | --- | --- | 




## API (Client - Server)

| Method | Endpoint | Protected | Usage | Response |
| --- | --- | --- | --- | --- |


## DB (Server Side)
  There should be HEAPS of tables

### Users
  | Column Name | Data Type |
  | --- | --- |
  | id | Integer |
  | user_name | String |
  | first_name | String |
  | last_name | String |
  | hash | text |

### Other stuff
  | Column Name | Data Type |
  | --- | --- |
  

### Attendees (Join Table M2M)

  Many Users attend Many Meetings

 | Column Name | Data Type |
 | --- | --- |
 | user_id | Integer |
 | meeting_id | Integer |

 ---
 

## Setup

Run the following commands in your terminal:

yarn start

yarn knex migrate:latest
yarn knex seed:run

## Heroku!!!

### Creating your app

Create your app with `heroku create [name]`

You can check that this was successful by running `heroku apps` to view a list of your apps


### Adding postgres

Add postgresql (hobby dev) to your app at `https://dashboard.heroku.com/apps/[APP NAME HERE]/resources`

Check that pg has been added by running `heroku addons` to ensure the postgresql db is on your app


### Deploying!

I have created several npm scripts that will be useful for deploying your app to heroku easily.

`npm run h:deploy` will push your local master branch to your heroku app

`npm run h:migrate` will run your knex migrations on your deployed heroku app

`npm run h:seed` will run your seeds on your deployed app

If ever you need to rollback, you can also just use `npm run h:rollback`
