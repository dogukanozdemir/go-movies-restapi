# Movies REST API with MongoDB GoLang

This project offers a simple REST API to perform CRUD operations on movies MongoDB.

![Rest API and MDB](https://www.codeproject.com/KB/database/1071823/image001.png)

# What is RESTful API?

REST is a set of architectural constraints, not a protocol or a standard. API developers can implement REST in a variety of ways.

When a client request is made via a RESTful API, it transfers a representation of the state of the resource to the requester or endpoint. This information, or representation, is delivered in one of several formats via HTTP: JSON (Javascript Object Notation), HTML, XLT, Python, PHP, or plain text. JSON is the most generally popular file format to use because, despite its name, it’s language-agnostic, as well as readable by both humans and machines. 

Something else to keep in mind: Headers and parameters are also important in the HTTP methods of a RESTful API HTTP request, as they contain important identifier information as to the request's metadata, authorization, uniform resource identifier (URI), caching, cookies, and more. There are request headers and response headers, each with their own HTTP connection information and status codes.

# Project Overview

These are all of the endpoints:
- **GET** a single movie with 'id' -> `/movies/:id`
  - Sample Response: 
  ```
  
    {"Id":"62c8410dadc8c4ae1fd089e9","Isbn":"tutlul123","name":"movie2","director":{"firstname":"gos","lastname":"movies"}}
    
  ```
- **GET**  all of the movies -> `/movies` 
  - Sample Response:
  ```
  [{"Id":"62c8410dadc8c4ae1fd089e9","Isbn":"tutlul123","name":"movie2","director":{"firstname":"gos","lastname":"movies"}},      {"Id":"62c84115adc8c4ae1fd089ea","Isbn":"tutlul1111123","name":"moviessss2","director":{"firstname":"goasdsads","lastname":"moasdavies"}}]
  ```
- **PUT** update a movie -> `/movies`
  - Sample Body:
  ```
            'Id' : id,
            'isbn' : isbn,
            'name' : name,
            'director' : {
                "firstname" : firstname,
                "lastname" : lastname
            }
  ```
  - Sample Response:
  ```
  {"Id":"62c84115adc8c4ae1fd089ea","Isbn":"asd","name":"asdd","director":{"firstname":"1123","lastname":"1333"}}
  ```
- **DELETE** a movie with 'id' -> `/movies/:id` 
  - Sample Response:
  ```
  {"message ":"Movie with Id 62c8410dadc8c4ae1fd089e9 deleted"}
  
  ```
-  **POST** create a movie -> `/movies`
    - Sample Body:
    ```
              'isbn' : isbn,
              'name' : name,
              'director' : {
                  "firstname" : firstname,
                  "lastname" : lastname
              }
    ```
    - Sample Response:
    ```
    {"Id":"62edc90cce2de380e4782f31","Isbn":"asda","name":"daad","director":{"firstname":"adda","lastname":"adad"}}
    ```
# Installation

Clone the repository into a directory of your choice
Run the command `go mod tidy` to download the necessary packages.

You'll need to add a .env file and add a MongoDB connection string with the name `MONGODB_URL` to access your collection.

# License

This project is licensed under the terms of the MIT license.
