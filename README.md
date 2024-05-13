# World Cup Database

### Objective

Build and query a database of World Cup games using PostgreSQL

### Directions To Run

1. Clone the directory
2. `cd` into the project directory
3. Run `psql -U postgres < worldcup.sql` in the terminal

Note: You may need to have a PostgreSQL database set up locally named postgres, if you set a database up under a different name change the command to include your db name instead `psql -U (your db name here) < worldcup.sql`

### Tasks

#### Part 1: Create Database
Create the database following the user stories below:

- You should create a database named worldcup

- You should connect to your worldcup database and then create teams and games tables

- Your teams table should have a team_id column that is a type of SERIAL and is the primary key, and a name column that has to be UNIQUE

- Your games table should have a game_id column that is a type of SERIAL and is the primary key, a year column of type INT, and a round column of type VARCHAR

- Your games table should have winner_id and opponent_id foreign key columns that each reference team_id from the teams table

- Your games table should have winner_goals and opponent_goals columns that are type INT

- All of your columns should have the NOT NULL constraint

#### Part 2: Insert the data

- Your two script (.sh) files should have executable permissions. Other tests involving these two files will fail until permissions are correct. When these permissions are enabled, the tests will take significantly longer to run

- When you run your insert_data.sh script, it should add each unique team to the teams table. There should be 24 rows

- When you run your insert_data.sh script, it should insert a row for each line in the games.csv file (other than the top line of the file). There should be 32 rows. Each row should have every column filled in with the appropriate info. Make sure to add the correct ID's from the teams table (you cannot hard-code the values)

#### Part 3: Query the database
- You should correctly complete the queries in the queries.sh file. Fill in each empty echo command to get the output of what is suggested with the command above it. Only use a single line like the first query. The output should match what is in the expected_output.txt file exactly, take note of the number of decimal places in some of the query results
