# JS-Backend-Rentbook-app
## TAMAN BUKU DIMAS
Backend Rentbook app using express.js and mysql

#### Prerequisite
---
1. Node.js - Download and Install [Node.js](https://www.nodejs.org) with NVM (Node Version Manager) - Simple bash script to manage multiple active node.js versions.
2. MySQL - Download and Install [MySQL](https://mysql.com) - Make sure it's running on the default port.
3. Postman - Download and Install [Postman](https://postman.com) - Implementation with postman latest version.

#### Installation
---

##### Clone 
$ git  clone https://github.com/DimasBayu24/JS-Backend-Rentbook-app.git

$ npm install

##### Configuration

DB_HOST= your database host

DB_USER= your username's database

DB_PASSWORD= your database password

DB_NAME= your database name

REQUEST_HEADERS= sensitive name for your req.headers

LENGTH_SALT= 20


#### Documentation
---
##### Routes

###### GET Method
* "/api/v1" => get list of all books
* "/api/v1/searh/(booktitle) => search book by the title
* "api/v1/availability" => get list of all available books
* "api/v1/sortbook" => get list all of books sorted by its title
* "api/v1/sortdate" => get list of all books sorted by its release date
* "api/v1/sortgenre" => get list of all books sorted by its genre
---
###### POST Method
* "api/v1/addbook" => post new book to database
* "api/v1/user/register" => register ID for more access
* "api/v1/user/login" => login with registered ID
---
###### PATCH Method
* "api/v1/rent/(id)" => rent a book from TAMAN-BUKU-DIMAS (if not rented yet)
* "api/v1/return/(id)" => return a book
* "api/v1/(id)" => update book's data
---
###### DELETE Method
* "api/v1/(id)" => delete book from database
---

{
  "name": "taman-buku-dimas",
  "version": "1.0.0",
  "description": "rent-book-app",
  "main": "app.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "nodemon  app.js"
  },
  "author": "dimasbayuseno@gmail.com",
  "license": "ISC",
  "dependencies": {
    "body-parser": "^1.19.0",
    "crypto": "^1.0.1",
    "dotenv": "^8.2.0",
    "express": "^4.17.1",
    "jsonwebtoken": "^8.5.1",
    "morgan": "^1.9.1",
    "mysql": "^2.18.1"
  }
}
