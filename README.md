# MiESt
Misskey Emoji Statistic

## Introduction

Goals of this project is a small python script that gets used emojis and reactions form one account and writes the data
into a database. To get a nice graphical view a frontend in form of some HTML files will be put out, so it is easy 
accessible.

## Project scope

The Project will contain four major parts:
    - The runtime, to poll the notes and reaction regularly to keep the server load spread out
    - The database (at the moment I am planning to use sqlite)
    - The backend, for handling all the Misskey API stuff
    - The front end, for writing down some HTML files, so they are easy accessible via a browser.

## TODO

### Set up script
To avoid using another conf-file, the idea is to have some sort of `miest-setup.py` that creates the database (setting
up the tables and stuff) and getting the user started in a dialog. Over this it should be possible to do changes if necessary.<br />
In a later stage this could be ramped up to be a full-fledged web interface with easy access for everyone.

### Runtime
Easy script that handles all the polling and the creating of the frontend HTML once a day. The entry point to run MiESt after the setup

### MiESt backend
Gets all the request stuff done onto the API and writing it into the database.<br />
In a later stage could be ramped up to an API, for easy access to the database.

### MiESt frontend
Queries the database and provides HTML files for the easy access of the Statistic.<br />
At the start it will provide some standard queries, on a later stage maybe a little bit of easy user customisation.

### Database
Contains four tables:
user <- Data of the user (e,g, Instance domain, username, token, etc.)
emojis <- database for the shortcode and the link to the according picture.
notes <- contains what emoji (identified by shortcode) has been used how many times. Together with the timestamp and the note id.

## TODO (haven't started programming yet)
- Write `miest-setup.py` for easy set up
- Set up a runtime (probably apscheduler)
- Rewrite the routines to get the notes from a set note id until now
- Rewrite routine to get the reactions until a set time until now
- Write routines to get several HTML files. At the moment planned:
  - Yesterday
  - Current week
  - Last week
  - Current month
  - Last month
  - Current year
  - Last year
  - Top 10 most used

## Feel free to add your thoughts
Nothing really happened yet, but while I go on with the project feel free to open a discussion to request something
or how to improve stuff.