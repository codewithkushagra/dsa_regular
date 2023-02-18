# DSA Regular

## Setting Up Django Project Locally using Docker

This guide will help you set up your Django project locally using Docker.

### Prerequisites
- Docker installed on your system
  - Installation guide: https://docs.docker.com/engine/install/

### Steps

1. Clone the repository using the following command:
```
git clone https://github.com/codewithkushagra/dsa_regular.git
```

2. Change directory into the cloned repository:
```
cd dsa_regular
```

3. Open the terminal and run the following command to build and start the required containers:
``` 
docker-compose -f local.yml up -d 
```

4. Verify that all containers are running properly by running the following command:
```
docker ps
```
You should see 2 containers:
- `dsa_regular_local_django` - the Django server
- `dsa_regular_local_postgres` - the Database server

5. In a new terminal, run the following commands to make migrations:
```
docker-compose -f local.yml run --rm django python manage.py makemigrations
```
```
docker-compose -f local.yml run --rm django python manage.py migrate
```

6. Once the setup is complete, go to:
```
0.0.0.0:8000/
```

### How to contribute
// TODO