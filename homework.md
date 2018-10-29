# SQL Homework

The local cinema are having a Marvel Movie Marathon! They have asked you to help maintain their database of movies with times and attendees.

## To access the database:

First, create a database called 'marvel'

```
# terminal
createdb marvel
```

Next, run the provided SQL script to populate your database:

```
# terminal
psql -d marvel -f marvel.sql
```

Use the supplied data as the source of data to answer the questions. Copy the SQL command you have used to get the answer, and paste it below the question, along with the result they gave.

## Questions

1.  Return ALL the data in the 'movies' table.
SELECT * FROM movies;

2.  Return ONLY the name column from the 'people' table
SELECT name FROM people;

3.  Oops! Someone at CodeClan spelled Rob's name wrong! Change it to reflect the proper spelling ('Robin Willson' should be 'Rob Wilson').
UPDATE people SET name = 'Rob Wilson' WHERE id =21;

4.  Return ONLY your name from the 'people' table.
SELECT name FROM people WHERE id = 6;

5.  The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.
DELETE FROM movies WHERE title = 'Batman Begins';

6.  Create a new entry in the 'people' table with the name of one of the instructors.
INSERT INTO people (name) VALUES ('Pavel');

7.  Nick Fury has decided to hijack our movie evening, Remove him from the table of people.
DELETE FROM people WHERE name = 'Nick Fury';

8.  The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this.
INSERT INTO movies (title, show_time) VALUES ('Avengers: Infinity War', '00:00');

9.  The cinema would also like to make the Guardians movies a back to back feature. Find out the show time of "Guardians of the Galaxy" and set the show time of "Guardians of the Galaxy 2" to start two hours later.
UPDATE movies SET show_time = '14:30' WHERE title = 'Guardians of the Galaxy 2';

## Extension

1.  Research how to delete multiple entries from your table in a single command.
DELETE from movies WHERE title = 'Iron Man' OR title = 'Iron Man 2' OR title = 'Iron Man 3';
