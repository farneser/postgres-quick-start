# PostgreSQL Quick Start

Simple start with postgresql with docker and pgadmin that you can you use in localhost

## Usage

### Run docker container

```bash
sudo docker-compose up -d
```

### PgAdmin

PgAdmin start on `http://localhost:5050`

Default user

* Login: `admin`
* Password: `admin`

### PgAdmin add server

You can add your local server with 4 steps

1. Go to `http://localhost:5050`
2. In object explorer
    1. Click on the "Servers" button
    2. Select "Register"
    3. Add "Server"
3. Add Server
    1. Enter any name of server 
    2. Go to tab "Connection"
    3. In field "Host name/address" enter `host.docker.internal`
    4. In field "Username" enter `postgres_user`
    5. In field "Password" enter `postgres_password`
    6. Select field "Save password?"
4. Enjoy

## Default connection string

### JBDC

``` postgresql
jdbc:postgresql://localhost:5432/postgresdb?user=postgres_user&password=postgres_password
```

### Entity framework

```efcore
Host=localhost;Port=5432;Database=postgresdb;Username=postgres_user;Password=postgres_password;IncludeErrorDetail=True"
```