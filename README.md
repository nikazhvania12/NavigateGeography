# NavigateGeography — A Website Created to Teach You All About Countries and Their Whereabouts

NavigateGeography is an interactive educational platform designed to make learning world geography engaging and accessible. It offers dynamic maps, country profiles, and data-driven insights on topics like water supply, resources, and population. Ideal for students, teachers, and curious minds.

## Requirements

- [Python 3.10 or higher](https://www.python.org/downloads/release/python-3100/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Node.js](https://nodejs.org/) (v16 or higher recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- [PostgreSQL](https://www.postgresql.org/) (used as the database backend)
- [pgAdmin 4](https://www.pgadmin.org/download/) (optional, for managing the database and running SQL scripts)

## Clone the Project

```bash
git clone https://github.com/nikazhvania12/NavigateGeography.git
```

## Configure the Project

NavigateGeography uses a PostgreSQL database that is already populated with necessary data.  
You’ll need to create a local PostgreSQL database to run the project fully.

The database configuration is located in `docker-compose.yaml` under `services → backend → environment`.

Update these values to match your local PostgreSQL setup:

```bash
DB_HOST=your_db_host
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_PORT=your_db_port
```

## Populate the Database

To finalize database setup, create the necessary tables and insert the initial data.  
In **pgAdmin 4**, open the Query Tool and run the contents of the following files:

- [Create Tables, Sequences, and Functions Script](./sql_create_scripts.txt)
- [Insert Data Script](./sql_insert_scripts.txt)

## Run the Project

Open your terminal and navigate to the cloned project:

```bash
cd NavigateGeography
```

To move between folders:

```bash
cd <your-folder-name>
cd ..
```

Use these commands to reach the project directory.  
Once there, your prompt should look like:

```bash
...\NavigateGeography>
```
or
```bash
~/NavigateGeography$
```

(depending on your OS and terminal)

Then run the project using Docker:

```bash
docker-compose up --build
```

This will start the frontend and backend on ports `3000` and `5000`, respectively.

If you want to change these ports or other settings, edit the [docker-compose.yaml](./docker-compose.yaml) file.

To stop the application:

```bash
docker-compose down
```
