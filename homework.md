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
--SELECT * FROM movies

2.  Return ONLY the name column from the 'people' table
--SELECT * FROM people

3.  Oops! Someone at CodeClan spelled Chae's name wrong! Change it to reflect the proper spelling ('Shae Nicholsun' should be 'Chae Nicholson').
--UPDATE people SET name = 'Chae Nicolson' WHERE name = 'Shae Nicholsun'

4.  Return ONLY your name from the 'people' table.
--SELECT name FROM people WHERE name = 'Jamie Paterson';

5.  The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.
--DELETE FROM movies WHERE title = 'Batman Begins';

6.  Create a new entry in the 'people' table with the name of one of the instructors.
--INSERT INTO people (name) VALUES ('Zvolt');

7.  Harrison Booth has decided to hijack our movie evening, Remove him from the table of people.
--DELETE FROM people WHERE name = 'Harrison Booth';

8.  The cinema has just heard that they will be holding an exclusive midnight showing of 'Captain Marvel'!! Create a new entry in the 'movies' table to reflect this.
--INSERT INTO movies (title, year, show_time) VALUES ('Captain Marvel', 2018, '12:00');

9.  The cinema would also like to make the Guardians movies a back to back feature. Find out the show time of "Guardians of the Galaxy" and set the show time of "Guardians of the Galaxy 2" to start two hours later.
--UPDATE movies SET show_time = '01:40' WHERE title = 'Guardians of the Galaxy 2';

## Extension

1.  Research how to delete multiple entries from your table in a single command.
--DELETE FROM movies WHERE year < 2017;



--UPDATE people SET name = 'Chae Nicolson' WHERE name = 'Shae Nicholsun'
--SELECT name FROM people WHERE name = 'Jamie Paterson';
--DELETE FROM movies WHERE title = 'Batman Begins';
--INSERT INTO people (name) VALUES ('Zvolt');
--DELETE FROM people WHERE name = 'Harrison Booth';
--INSERT INTO movies (title, year, show_time) VALUES ('Captain Marvel', 2018, '12:00');
--UPDATE movies SET show_time = '01:40' WHERE title = 'Guardians of the Galaxy 2';
--DELETE FROM movies WHERE year = 2017;



--SELECT * FROM movies
--SELECT * FROM people
