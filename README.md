# restaurantsApp

this is a basic API built with rails.

The application has been built with the MVC design pattern and REST convections.

## Pre-Requisites
In order to use this repository you will need the following:



- Operating System **(Windows `10+`, Linux `3.8+`, or MacOS X `10.7+`)**
- RAM >= 4GB
- Free Space >= 2GB

## Built With
This application has been built with the following tools:

![ruby](https://img.shields.io/badge/Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white)
![sqlite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)


- **Ruby `v2.7.+`**
- **SQlite3 `v1.6`**
- **ActiveRecord `v7.0.4`**
- **Rake `v13.0.6`**
- **Puma `v6.1`**
- **rerun `v0.14`**
- **Rails ``**
- **ERB `v4.0`**

## Setup
You can setup this repository by following this manual

1. Clone the repository and navigate to restaurantApp folder.
    ```{shell}
   git clone https://github.com/CaseyOchieng/phase-4-code-challenge
   ```
2. Ensure the ruby gems are setup in your machine
    ```{shell}
   bundle install
   ```
3. Perform any pending database migrations
   ```{shell}
   rake db:migrate
   ```
4. You cant also seed some sample data with
   ```{shell}
   rake db:seed

5. Run the server
    ```{shell}
    rails server or rails s 
    ```
6. Open the application from your browser
    ```
   http://localhost:3000
   ```
   
## Application
This application is a simple web API that allows users to:

- view all the restaurants.
- view a single restaurant with its available pizzas.
- Delete a restaurant.
- view all the pizzas.
- add a restaurant pizza with the price.


### MODELS
Database schema definitions.



####  restaurants table

| COLUMN      | DATA TYPE  | DESCRIPTION                                  | 
|-------------|------------|----------------------------------------------|
| id          | Integer    | Unique identifier.                           |
| name        | String     | The name of the restaurant                   |
| address     | String     | The address of the restaurant.               |
| timestamp   | Date       | timestamp restaurant was created and updated.|



#### pizzas table
| COLUMN        | DATA TYPE | DESCRIPTION                               | 
|---------------|-----------|-------------------------------------------|
| id            | Integer   | Unique identifier.                        |
| name          | String    | pizzas name.                              |
| ingredients   | String    | pizzas ingredients                        |
| timestamp     | Date      | timestamp pizza was created and updated.  |

#### restaurant pizzas table
| COLUMN        | DATA TYPE | DESCRIPTION                                       | 
|---------------|-----------|---------------------------------------------------|
| id            | Integer   | Unique identifier.                                |
| restaurant_id | Integer   | foreign key restaurant identification             |
| pizza_id      | Integer   | foreign key pizza identification                  |
| timestamp   | Date        | timestamp restaurant pizza was created and updated.|




### ROUTES

1. GET ``` /restaurants ``` 
    ## RESPONSE SAMPLE

  
2. GET ```  /restaurants/:id ``` 
    ## RESPONSE SAMPLE if restaurant is found
   


    ## RESPONSE SAMPLE if restaurant is not found

  

3. DELETE ``` /restaurants/:id ``` 

    ## RESPONSE SAMPLE if restaurant is delete is successful found

    
    ## RESPONSE SAMPLE if restaurant is not found



4. GET ``` /pizzas ``` 

    ## RESPONSE SAMPLE


5. POST ``` /restaurant_pizzas ```

   ```{json}
   ## REQUEST BODY SAMPLE
        {
        "price": 5,
        "pizza_id": 1,
        "restaurant_id": 3
        }
   ```

   ## RESPONSE SAMPLE if the data was valid

    ```
        {
        "id": 1,
        "name": "Cheese",
        "ingredients": "Dough, Tomato Sauce, Cheese"
        }
    ```

    ## RESPONSE SAMPLE if the data was not valid

  


## Author
This repository is maintained by:

- [Casey Ochieng](https://github.com/CaseyOchieng) 