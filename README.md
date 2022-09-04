<p align="left">
  <img height="150" src="./client/src/media/logonavbar.png" />
</p>


__DEPLOY LINK__: __https://bsale2.vercel.app/__

## Objective:
Create an E-commerce that is able to display products based in their category, 
utilizing the provided database for its development. 
You must also implement a search function where the results must arrive already filtered to the client



## Technologies and Tools

- JavaScript 
- NodeJS 
- ExpressJS
- Sequelize ORM

## Documentation

Sequelize Model Definitions:

 Product:
id: Type: UUID  
name: Type: String
price: Type: Float
url_image: Type: String
discount: Type: Integer
category: Type: Integer

Category:
id: Type: Integer
name: Type: String
Routes:
 Base URL: https://bsale-miniati.herokuapp.com

Product routes: “/product”
GET all products:
GET /product/
Returns an array of  Product type objects
Example: https://bsale-miniati.herokuapp.com/product/


GET matching products
GET /product/search?name={name}
Receives a name through query
Returns an array of Product type objects whose property “name” matches the input. 
Example: https://bsale-miniati.herokuapp.com/product/search?name=pisco

POST filter by category
POST /product/filter 
Receives a json type object through body, with the id of the desired categories
 {“categories”: {desired categories}} 
Returns an array of Product type objects whose property “category” matches the desired category
Example: https://bsale-miniati.herokuapp.com/product/filter, 
{“categories”: 2}

Category routes: “/category”
GET all categories:
GET /category/
Returns an array of Category type objects
Example: https://bsale-miniati.herokuapp.com/category/

