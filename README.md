# E-Commerce-Back-End
## ![badge](https://img.shields.io/static/v1?label=Licence&message=MIT&color=blue&style=plastic)
## Table of Contents
- [Description](#Description)
- [Installation Instructions](#Installation-Instructions)
- [Usage Information](#Usage-Information)
- [Contribution Guidelines](#Contribution-Guidelines)
- [Test Instructions](#Test-Instructions)
- [Video Link](#Video-Link)
- [GitHub Page](#GitHub-Page)
- [Questions](#Questions)
## Description
This is E-Commerce Back End, a command line app for online store owners to create, read, update, and delete (CRUD) information about their products. Users can perform CRUD actions on categories, products, and tags. Some seed data is provided for users to test out the routes and functionalities.
## Installation Instructions
To install required npm packages:
```
npm i
```
To create the database:
```
mysql -u root -p < db/schema.sql
```
To pre-populate the database with some entries:
```
npm run seed
```
To start the app:
```
npm start
```
## Usage Information
The user can access different routes using different methods and urls to send specific requests to the back end:

### Main Routes
Category route
```
http://localhost:3001/api/categories/
```
Tag route
```
http://localhost:3001/api/tags/
```
Product route
```
http://localhost:3001/api/products/
```

By appending to the aforementioned urls, different requests can be sent:

### Sub Routes
Read all entries from the table
```
/
method: GET
```
Read one entry from the table
```
/:id
method: GET
```
Create a new entry
```
/
method: POST
```
Update an entry from the table
```
/:id
method: PUT
```
Delete an entry from the table
```
/:id
method: DELETE
```

When an ID is required for some of the above methods and the provided ID is not within the database, the response will be a 404 error message. When fetching information for the category(s), all relevant products will display. When fetching information for tags or products, the relevant products and tags will display as well. When using the POST and PUT methods, a JSON object needs to be sent as the request body. Here are some examples:

Category Format
```
{
    "category_name": "Coats"
}
```
Tag Format
```
{
    "tag_name": "geeky"
}
```
Product Format
```
{
    "product_name": "Basketball",
    "price": 200.00,
    "stock": 3,
    "tagIds": [1, 2, 3, 4]
}
```

## Contribution Guidelines
N/A
## Test Instructions
```
N/A
```
## Video Link
https://drive.google.com/file/d/1Th8-NhNg-7kVfQbgEKfjmYx35ZSq2MiS/view?usp=sharing
## GitHub Page
https://github.com/runescape11111/E-Commerce-Back-End
## Questions
GitHub profile: github.com/runescape11111/

Email: olivershih@gmail.com
