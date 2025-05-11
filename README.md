# NavigateGeography, a Website, Created to teach you all About Countries and their Whereabouts

NavigateGeography is an interactive educational platform designed to make learning world geography engaging and accessible. It offers dynamic maps, country profiles, and data-driven insights on topics like water supply, Resources, and Population. Ideal for students, teachers, and curious minds.

## Requirements

- [Python 3.10](https://www.python.org/downloads/release/python-3100/)  or higher
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Node.js](https://nodejs.org/) (version 16 or higher recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- [PostgreSQL](https://www.postgresql.org/) (used as the database backend)
- [pgAdmin 4](https://www.pgadmin.org/download/) (optional, for managing the database via a GUI and handle scripts)

## Clone the Project
```bash
git clone https://github.com/nikazhvania12/NavigateGeography.git
```
NavigateGeography uses a PostgreSQL Database, which is already populated with necessary data. You will need to created a local PostgreSQL database to fully run this project.
The configuration of said database is available in docker-compose.yaml (Navigate to services -> backend -> enviroment).
```bash
DB_HOST=your_db_host
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_PORT=your_db_port
```
Modify the enviroment section to match the properties of your created PostgreSQL database.

## Populate Database
To finalize Database Modification, you will need to create neccesarry tables/functions and insert valid data. in pgAdmin 4, run a query tool and paste the contents of two files provided below:
- [Create Tables, Sequences and Functions](./sql_create_scripts.txt)
- [Insert Data](./sql_insert_scripts.txt)
