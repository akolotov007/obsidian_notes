all commands should be written in UPPERCASE
strings are in ' '
always finish your commands with `;`
`-- comment`
`/* */` multiline comment

```mysql
CREATE DATABASE record_company;
```
- creates a database, but doesn't  yet use it

```mysql
USE record_company;
```
- use this database

```mysql
CREATE TABLE test (
test_column INT
);
```
- create column and define data type

```mysql
ALTER TABLE test 
ADD another_column VARCHAR(255);
```
- create a string column w/ max length of 255\

```mysql
DROP TABLE test;
```

## Beginning

Lets create a table called bands, which will have 1 column for their name. Also make it so that the table HAS to have a name: with `NOT NULL`
```mysql
create TABLE bands(
name VARCHAR(255) NOT NULL
);
```
 also we should add an ID to every band so that we don't mix up the names of the bands (if they have the same name)

```mysql
create TABLE bands(
// ID INT NOT NULL AUTO_INCREMENT,
name VARCHAR(255) NOT NULL
);
```

we also should define what the primary key is, in this case `ID`

```mysql
create TABLE bands(
ID INT NOT NULL AUTO_INCREMENT,
name VARCHAR(255) NOT NULL,
PRIMARY KEY (ID)
);
```

Great, now lets create an album table:

```mysql
CREATE TABLE albums (
ID INT NOT NULL AUTO_INCREMENT,
name VARCHAR(255) NOT NULL,
release_year INT
);
```
- *we don't know when an album might release, so we can define it as INT but not w/ NOT NULL *
- I also want to associate the band name to the album, by referencing the bands table

```mysql
CREATE TABLE albums (
ID INT NOT NULL AUTO_INCREMENT,
name VARCHAR(255) NOT NULL,
release_year INT,
band_id INT NOT NULL,
PRIMARY KEY (ID),
FOREIGN KEY (band_id) REFERENCES bands(id)
);
```
- foreign key = any key that references another table outside of the current table

Now let's add some bands into the "bands" table, with INSERT INTO

```mysql
INSERT INTO bands (name)
VALUES ("Iron Maiden"), ('Avenged Sevenfold'), ('Ankor');
```
- INSERT INTO (table) (table column{s}) followed by the VALUES to be added to those columns 

Now lets SELECT some columns from that "bands" table that we created

```mysql
SELECT * FROM bands;
```
- *select (columns) from (table)*
```mysql
SELECT * FROM bands LIMIT 2; 
```
- limiting the results to the first 2 bands

we can also add aliases the columns in our tables so that it will be easier for us to query them  
```mysql
SELECT ID AS "ID", name as "Band Name"
FROM bands;

SELECT * FROM bands ORDER BY name;
							--   ^DESC / if in descending order
-- also order by a column, this case name / result alphabetical 
```

Now lets add some albums to the "albums" table

```mysql
INSERT INTO albums (name,release_year,band_id)
VALUES ('The Number of the Beasts', 1985, 1),
	   ('Power Slave', 1984,1),
       ('Nightmare', 2018, 2),
       ('Nightmare', 2010, 3),
       ('Test Album', NULL, 3);
```
- looking at the "bands" table, we took the ID generated for each band and wrote it in for each of these albums

```mysql
SELECT name FROM albums;
```
- shows "name" column in "albums" table
	- *nightmare shows up twice*
		- we want to see distinct names

```mysql
SELECT DISTINCT name FROM albums;
```

Oh no! we gave the wrong release year for one of the albums, we have to change it 

```mysql
 UPDATE ALBUMS
 SET release_year  = 1982
// WHERE ID = 1;
```

WHERE can be used practically after any SQL statement, such as picking out albums that were released before 2000

```mysql
SELECT * FROM albums WHERE release_year < 2000; 
```

we can also find any strings that contain 

```mysql
SELECT * FROM albums
WHERE name LIKE '%er%';
-- % wildcard, 
```