# Ducatus Codility Test

## Instructions
   Follow the URL and req body requirements. You have 1 hour to complete the task. 

## Requirements

NodeJS (Express)
MongoDB

## Steps
   1.) Create a database that has a User Collection with ff: (MongoDB) 
   
           {name: "john", age: 20, status: "active"}
           {name: "gina", age: 35, status: "active"}
           {name: "jane", age: 31, status: "not active"}
   2.) Create a local node server that will brodcast the User Document via API GET 
        
            URL: localhost:8080/user
   3.) Create POST API for creating new user with a default status of "active"
            
            URL: localhost:8080/user-add
  			   req body: { name: "sample name", age: 'sample age' }
   4.) Create PUT endpoint that will update status to "not active" or "active" of a specific user via id field.
       Negate the new status depending on its original status value from the database. 
   
          URL: localhost:8080/user-status
  			 req body: { userID: userID }
            
##  Time: 1 hr
##  Good Luck!!
