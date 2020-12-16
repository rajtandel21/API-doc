# API-Document
The document will cover the api document, the tables and the type of database used.

We decided to go with a SQL database. This was because our data does not have much variance, as most users have to enter the same data. The tables also have a relation to each other so SQL seems the most appropriate approach.

## Person Table

Id | Name | Age | NumOfPerson
---|------|-----|------------
P1 | Bob  | 50  | 3


## House Table

ID | Owner | Address 
---|-------|---------
H1 | P1   | A1


## Address table

ID | Postcode | Street Address
---|----------|---------------
A1 | W3DH     | 30 Baker street


## REST API

Path | HTTP Verb | Action
-----|-----------|--------
/user | POST | Create
/house | GET | Index
/user | GET | Show

## Query Params

Below are some examples of how you would want to use the API.

> Get people in our neighbourhood within certain age brackets and with specific household sizes

`/user?postcode=w3dh&minage=20&maxage=50&household=3`

Data returned:

`{name: 'bob', age@ 50, address: '30 Backer Street', household: 3}`

> Get a house, it’s address and owner

`/house?id=h1`

Data returned:

`{name: 'bob', address: {postcode: 'W3DH', street: '30 Backer Street'}}`
