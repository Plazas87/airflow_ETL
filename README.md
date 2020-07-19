# Airflow toturial
Simple data pipeline using Airflow

## Requirements

* docker
* pandas
* psycopg2 
* airflow

## Installation

```bash
python -m pip install -r requirements.txt
```

## Start a postgres instance

To run the app in development mode, execute:
```bash
docker run --name postgres_db -e POSTGRES_PASSWORD=postgres -e POSTGRES_USER=airflow -p 5432:5432 -d postgres
```

## Start the web server and scheduler
```bash
airflow webserver -p 8080
airflow scheduler
```
and then open `http://localhost:8080`
