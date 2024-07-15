# 0x01. NoSQL


### Project Information
- **Project Name:** 0x01. NoSQL
- **Domain:** Back-end
- **Specialization:** NoSQL
- **Technology:** MongoDB


## Resources
### Read or Watch:
1. [NoSQL Databases Explained](https://example.com)
2. [What is NoSQL?](https://example.com)
3. [MongoDB with Python Crash Course - Tutorial for Beginners](https://example.com)
4. [MongoDB Tutorial 2: Insert, Update, Remove, Query](https://example.com)
5. [Aggregation](https://example.com)
6. [Introduction to MongoDB and Python](https://example.com)
7. [mongo Shell Methods](https://example.com)
8. [Mongosh](https://example.com)

## Learning Objectives
By the end of this project, you should be able to explain:
- What NoSQL means
- Differences between SQL and NoSQL
- What ACID is
- What document storage is
- Types of NoSQL databases
- Benefits of NoSQL databases
- How to query, insert, update, and delete information in a NoSQL database
- How to use MongoDB

## Requirements
### MongoDB Command File
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using MongoDB (version 4.2)
- Files must end with a new line
- The first line of all files should be a comment: `// my comment`
- A `README.md` file at the root of the project folder is mandatory
- The length of files will be tested using `wc`

### Python Scripts
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using Python3 (version 3.7) and PyMongo (version 3.10)
- Files must end with a new line
- The first line of all files should be exactly `#!/usr/bin/env python3`
- A `README.md` file at the root of the project folder is mandatory
- Code should use the `pycodestyle` style (version 2.5.*)
- The length of files will be tested using `wc`
- All modules should have documentation
- All functions should have documentation
- Code should not be executed when imported (use `if __name__ == "__main__":`)

## More Info
### Install MongoDB 4.2 on Ubuntu 18.04
Official installation guide:

```bash
$ wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | apt-key add -
$ echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" > /etc/apt/sources.list.d/mongodb-org-4.2.list
$ sudo apt-get update
$ sudo apt-get install -y mongodb-org
$ sudo service mongod status
$ mongo --version
$ pip3 install pymongo
```

Potential issue if documents creation doesn’t work:
```bash
$ sudo mkdir -p /data/db
```

### Use “container-on-demand” to run MongoDB
- Ask for container Ubuntu 18.04 - MongoDB
- Connect via SSH or WebTerminal
- Start MongoDB in the container:
  ```bash
  $ service mongod start
  $ cat 0-list_databases | mongo
  ```

## Tasks

### 0. List all databases
**File:** `0-list_databases`

### 1. Create a database
**File:** `1-use_or_create_database`

### 2. Insert document
**File:** `2-insert`

### 3. All documents
**File:** `3-all`

### 4. All matches
**File:** `4-match`

### 5. Count
**File:** `5-count`

### 6. Update
**File:** `6-update`

### 7. Delete by match
**File:** `7-delete`

### 8. List all documents in Python
**File:** `8-all.py`

### 9. Insert a document in Python
**File:** `9-insert_school.py`

### 10. Change school topics
**File:** `10-update_topics.py`

### 11. Where can I learn Python?
**File:** `11-schools_by_topic.py`

### 12. Log stats
**File:** `12-log_stats.py`