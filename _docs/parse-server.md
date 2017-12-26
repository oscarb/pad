---
title: Parse Server
published: true
tags:
  - development
---

# Parse server

## Install

### Windows

```
npm install -g parse-server mongodb-runner
```

If MongoDb fails, [download MongoDb](https://www.mongodb.com/download-center#production).

## MongoDb

* Create the folder: C:\data\db\ where MongoDB will store database files
* Add to path: `set PATH=%PATH%;C:/Program Files/MongoDB/Server/3.2/bin/`

### Start database

    "C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --dbpath "d:\test\mongo db data"

### Connect to MongoDb

    "C:\Program Files\MongoDB\Server\3.4\bin\mongo.exe

## Resources

* [Installing your own parse-server on Windows](https://medium.com/@cristi_ursachi/installing-your-own-parse-server-on-windows-b2c7a2498d19#.1qmcj7xkn)
* [Install MongoDB Community Edition on Windows — MongoDB Manual 3.4](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/)


## Relationships

Referencing on the one-side, many-side or both?

Denormalize fields into the one or many side
Updating denormalized values are slower, more expensive and not atomic.


1. Favor embedding unless there is a compelling reason not to
2. Needing access to an object on its own is reason not to embed it
3. Arrays should not grow without a bond. Don't embed if there are more than hundreds on the many side. IF there are thousands on the many side, don't use an array of pointers.
4. Use application-level joins as they are barely more expensive than server-side joins in relational databases.
5. Consider write/read ratio when denomralizing. Fields that are only read but rarely updated to are good candidates for denormalization. 
6. Structure the data to match the ways the application queries and updates it.


Two-way referencing
 - Requires two updates


* Pointers
  - Pros
    * Use include on query
    * Simple, easy to use
    * More typesafe than arrays
    * Scales indefinitely
  - Cons
    * Limited to only one-to-many relationships
    * Gettings objects on both sides requires two calls
    * Conceptually might feel counter-intutive (querying on the wrong side)
* Arrays
  - Pros
    * Conceptually makes total sense, easy to use
    * Include on query
    * Works for both one-to-many and many-to-many relationships
    * Good when the _many_ is a predictable size
    * Supports order
  - Cons
    * Not typesafe
    * Not going to scale to large relationships
* Parse Relation
  - Pros
    * More scalable than arrays for large relationships
    * Able to restrict queries for subsets of data
  - Cons
    * Difficult conceptually
    * Include on queries not supported
    * Does not support order
* Join Table 
  - Pros
    * Meta-data for relationships
    * Just as scalable as Pointers
    * Just as scalable as Parse Relation
    * Conceptually similar to traditional detabase development
  - Cons
    * Create and maintain own join table


### One-to-one

Embedded vs referencing

Embedding is better for...

Small subdocuments
Data that does not change regularly
When eventual consistency is acceptable
Documents that grow by a small amount
Data that you’ll often need to perform a second query to fetch Fast reads
References are better for...

Large subdocuments
Volatile data
When immediate consistency is necessary
Documents that grow a large amount
Data that you’ll often exclude from the results
Fast writes

https://stackoverflow.com/a/27247579/6131896

### One-to-many

A blog post has many comments
A comment can only belong to one blog post
Customer has many orders

* Is the amount of many-objects predictable and not too many?
  - If yes, go for arrays
  - If no, go for pointers in the many-object
  
Should the objects on the many side be accessed separately or only in the context of the parent object?

What is the ratio of updates to reads for a particular field?
  
   
#### One-to-few

Array of embedded documents


#### One-to-many

Array of pointers or part-reference on the many-side


#### One-to-squillions

Use parent-reference on the many-side


#### Pointers

Comment
 - Text
 - Author 
 - BlogPost

Query for all comments...
"Get all comments where post is blog post X"

Query for post that a comment belongs to
...

#### Arrays

BlogPost 
 - Text
 - Author
 - Comments

Query for all comments

Query for blog post that comment belongs to 


### Many-to-many

Users following each other
Students and teachers
Sales persons and Accounts

If the relationships requires meta-data, use join tables otherwise Parse Relation

#### Parse Relation

Create...

Query all accounts for a gien person


Query all persons for a given account

#### Join Table


When meta-data is required for the relationships

Users following users

Creating...


Querying does Bob follow Eve...


## Hosting

### Parse/Node

Name | Database storage | Requests/second | Price   | Notes
-----|------------------|-----------------|---------|-----------
[Back4App](https://www.back4app.com/) | 0.5 GB | 10 | Free | 1 Cloud code job
[Buddy](https://buddy.com/) | ? | 30 | Free | $100 USD per additional 10 rps per month
[Heroku](https://www.heroku.com/) | 10K rows | ? | Free | -
[Google Cloud Platform](https://cloud.google.com/) | ? | ? | ? | -
[Red Hat OpenShift Online](https://www.openshift.com/pricing/index.html) | 1GiB | 1GiB Memory  | Free | -

### MongoDb

Name | Database storage | Price   | Notes
-----|------------------|---------|---------
[mLab](https://mlab.com/) | 0.5 GB | Free | -


## Push notifications

* [OneSignal](https://onesignal.com/)

## Back4App

### CLI 

Command | Description
--------|-------------
`configure accountkey` | Configure account to use
`new` | Create a new app or add cloud code to an existing app 
`deplpy` | Deploy code
`list` | View all linked apps
`develop <App Name>` | Watch for any updates, deploy them and see live stream of Cloud Code logs.

Resources
* [Command Line Interface to Parse Server](https://blog.back4app.com/2017/01/20/cli-parse-server/)

## How-to

* [How to query an 'Object' type field in parse](https://stackoverflow.com/questions/31306318/how-to-query-an-object-type-field-in-parse)
* [How to Query based on a Pointer on Parse Server](https://designingforscale.com/query-on-a-parse-pointer/)
