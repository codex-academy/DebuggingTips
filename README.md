# Debugging Tips

A large part of a software developers job is to find problems. To find problems in existing applications and to minimize problems in applications.

In this session we will look at tips, tricks and techniques for tracking down problems in our applications.

## We will look at:

* How to read error messages
* Failing tests
* Silent failures

## How to track down errors:
* Understanding the big picture
* What areas in the application is error prone
* What clue do we have?

## Analyzing stack traces:
* Which code is yours?
* At which line is the error?
* Why could things go wrong at that line?

## Isolating an issue:
* Remove code - check if it still fails
* Put code back until the error happens again
* Look at lines before & after the problem

## Debugging tools
* Chrome developer tools - break points
* print things to the console.
* break problem down into components
* use log files - with various log levels

#Setup

## Create a database

```sql
CREATE DATABASE debugging_tips;
CREATE USER debugger@localhost IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON debugging_tips.* TO debugger@localhost;
FLUSH PRIVILEGES;
```

## Create tables

```sql
create table issues (
  id int not null auto_increment,
  heading char(100) not null,
  description text,
  primary key(id)
);
```

## Install the dependencies

Using: `npm install`

Run the application using: `nodemon index.js`

 

 



