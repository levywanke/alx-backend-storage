Got it! Below is the `README.md` file for your project without any code.

### README.md

```markdown
# Redis Basics

## Description

This project involves working with Redis, a powerful in-memory data structure store, used as a database, cache, and message broker. The tasks in this project will help you understand how to use Redis for basic operations and as a simple cache.

## Learning Objectives

- Understand basic operations in Redis.
- Learn how to use Redis as a simple cache.
- Get familiar with Redis commands and their Python equivalents.
- Implement decorators to enhance functionality in a Redis context.

## Requirements

- All files are interpreted/compiled on Ubuntu 18.04 LTS using Python 3 (version 3.7).
- All files should end with a new line.
- A `README.md` file, at the root of the folder of the project, is mandatory.
- The first line of all your Python files should be exactly `#!/usr/bin/env python3`.
- Your code should use the `pycodestyle` style (version 2.5).
- All modules should have documentation.
- All classes should have documentation.
- All functions and methods should have documentation.
- All functions and coroutines must be type-annotated.

## Setup

1. **Install Redis on Ubuntu 18.04**
   ```sh
   sudo apt-get -y install redis-server
   ```

2. **Install Redis Python client**
   ```sh
   pip3 install redis
   ```

3. **Configure Redis**
   ```sh
   sed -i "s/bind .*/bind 127.0.0.1/g" /etc/redis/redis.conf
   ```

4. **Start Redis server**
   ```sh
   sudo service redis-server start
   ```

## Tasks

### 0. Writing strings to Redis
Create a `Cache` class with a method to store data in Redis.

### 1. Reading from Redis and recovering original type
Enhance the `Cache` class with methods to retrieve data from Redis and convert it back to its original type.

### 2. Incrementing values
Implement a decorator to count how many times methods of the `Cache` class are called.

### 3. Storing lists
Implement a decorator to store the history of inputs and outputs for a particular function in Redis.

### 4. Retrieving lists
Create a function to display the history of calls of a particular function, including its inputs and outputs.

## Usage

To use the `Cache` class and its methods, import it into your script and create an instance. Use the instance to store and retrieve data from Redis.
