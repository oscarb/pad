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
