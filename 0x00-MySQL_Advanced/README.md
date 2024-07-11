# MySQL Advanced Project

## Table of Contents
1. [Concepts](#concepts)
2. [Resources](#resources)
3. [Learning Objectives](#learning-objectives)
4. [Requirements](#requirements)
5. [Usage](#usage)
6. [Tasks](#tasks)

## Concepts
For this project, you will need to understand the following concepts:
- Advanced SQL

## Resources
Read or watch:
- [MySQL cheatsheet](https://devhints.io/mysql)
- [MySQL Performance: How To Leverage MySQL Database Indexing](https://www.percona.com/blog/2017/02/23/mysql-performance-how-to-leverage-mysql-database-indexing/)
- [Stored Procedure](https://dev.mysql.com/doc/refman/5.7/en/stored-routines.html)
- [Triggers](https://dev.mysql.com/doc/refman/5.7/en/triggers.html)
- [Views](https://dev.mysql.com/doc/refman/5.7/en/views.html)
- [Functions and Operators](https://dev.mysql.com/doc/refman/5.7/en/functions.html)
- [Trigger Syntax and Examples](https://dev.mysql.com/doc/refman/5.7/en/trigger-syntax.html)
- [CREATE TABLE Statement](https://dev.mysql.com/doc/refman/5.7/en/create-table.html)
- [CREATE PROCEDURE and CREATE FUNCTION Statements](https://dev.mysql.com/doc/refman/5.7/en/create-procedure.html)
- [CREATE INDEX Statement](https://dev.mysql.com/doc/refman/5.7/en/create-index.html)
- [CREATE VIEW Statement](https://dev.mysql.com/doc/refman/5.7/en/create-view.html)

## Learning Objectives
By the end of this project, you should be able to explain the following without any external help:
- How to create tables with constraints
- How to optimize queries by adding indexes
- What is and how to implement stored procedures and functions in MySQL
- What is and how to implement views in MySQL
- What is and how to implement triggers in MySQL

## Requirements
- All files will be executed on Ubuntu 18.04 LTS using MySQL 5.7 (version 5.7.30).
- All files should end with a new line.
- All SQL queries should have a comment just before (i.e., syntax above).
- All files should start with a comment describing the task.
- All SQL keywords should be in uppercase (SELECT, WHERE, etc.).
- A `README.md` file, at the root of the folder of the project, is mandatory.
- The length of your files will be tested using `wc`.

## Usage
### Running MySQL
Use "container-on-demand" to run MySQL:
1. Ask for container Ubuntu 18.04 - Python 3.7.
2. Connect via SSH or WebTerminal.
3. Start MySQL:
    ```sh
    $ service mysql start
    * MySQL Community Server 5.7.30 is started
    ```

### Importing a SQL dump
1. Create the database:
    ```sh
    $ echo "CREATE DATABASE hbtn_0d_tvshows;" | mysql -uroot -p
    Enter password:
    ```
2. Import the dump:
    ```sh
    $ curl "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/274/hbtn_0d_tvshows.sql" -s | mysql -uroot -p hbtn_0d_tvshows
    Enter password:
    ```

## Tasks

### 0. We are all unique!
- **File:** `0-uniq_users.sql`
- **Description:** Write a SQL script that creates a table `users` with attributes:
  - `id` (integer, never null, auto increment, primary key)
  - `email` (string, never null, unique)
  - `name` (string)
- **Command to run:**
    ```sh
    $ cat 0-uniq_users.sql | mysql -uroot -p
    ```

### 1. In and not out
- **File:** `1-country_users.sql`
- **Description:** Write a SQL script that creates a table `users` with attributes:
  - `id` (integer, never null, auto increment, primary key)
  - `email` (string, never null, unique)
  - `name` (string)
  - `country` (enumeration of countries: US, CO, TN, never null, default US)
- **Command to run:**
    ```sh
    $ cat 1-country_users.sql | mysql -uroot -p
    ```

### 2. Best band ever!
- **File:** `2-fans.sql`
- **Description:** Write a SQL script that ranks country origins of bands, ordered by the number of (non-unique) fans. Import the table dump: `metal_bands.sql.zip`.
- **Command to run:**
    ```sh
    $ cat metal_bands.sql | mysql -uroot -p
    $ cat 2-fans.sql | mysql -uroot -p
    ```

### 3. Old school band
- **File:** `3-glam_rock.sql`
- **Description:** Write a SQL script that lists all bands with Glam rock as their main style, ranked by their longevity. Import the table dump: `metal_bands.sql.zip`.
- **Command to run:**
    ```sh
    $ cat metal_bands.sql | mysql -uroot -p
    $ cat 3-glam_rock.sql | mysql -uroot -p
    ```

### 4. Buy buy buy
- **File:** `4-store.sql`
- **Description:** Write a SQL script that creates a trigger that decreases the quantity of an item after adding a new order.
- **Command to run:**
    ```sh
    $ cat 4-init.sql | mysql -uroot -p
    $ cat 4-store.sql | mysql -uroot -p
    ```

### 5. Email validation to sent
- **File:** `5-valid_email.sql`
- **Description:** Write a SQL script that creates a trigger that resets the attribute `valid_email` only when the email has been changed.
- **Command to run:**
    ```sh
    $ cat 5-init.sql | mysql -uroot -p
    $ cat 5-valid_email.sql | mysql -uroot -p
    ```

### 6. Add bonus
- **File:** `6-bonus.sql`
- **Description:** Write a SQL script that creates a stored procedure `AddBonus` that adds a new correction for a student.
- **Command to run:**
    ```sh
    $ cat 6-init.sql | mysql -uroot -p
    $ cat 6-bonus.sql | mysql -uroot -p
    ```

### 7. Average score
- **File:** `7-average_score.sql`
- **Description:** Write a SQL script that creates a stored procedure `ComputeAverageScoreForUser` that computes and stores the average score for a student.
- **Command to run:**
    ```sh
    $ cat 7-init.sql | mysql -uroot -p
    $ cat 7-average_score.sql | mysql -uroot -p
    ```

### 8. Optimize simple search
- **File:** `8-index_my_names.sql`
- **Description:** Write a SQL script that creates an index `idx_name_first` on the table `names` and the first letter of `name`. Import the table dump: `names.sql.zip`.
- **Command to run:**
    ```sh
    $ cat names.sql | mysql -uroot -p
    $ cat 8-index_my_names.sql | mysql -uroot -p
    ```