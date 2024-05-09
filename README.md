## airflow-local

This repo created a docker version of standalone local airflow as the development environment.
Please refer to
1. https://airflow.apache.org/docs/apache-airflow/stable/start.html
2. https://harshalpagar.medium.com/running-airflow-with-docker-on-developer-environment-9c1c9559668c

create a folder `dags` to start developing, and it will be automatically sync with docker container if using `--watch` flag.

## user and password
user: admin
password can be found in `/opt/airflow/standalone_admin_password.txt`.

## How to run
use `docker compose` to control up and down.
typical command could be
`docker compose dev up --watch`
`docker compose down`

## Issues for local pypi installation on macos
I met `google-re2` issue in [this](https://stackoverflow.com/questions/76701323/trying-to-download-apache-airflow-with-pip-but-error-pops-up-when-building-whee) link.
I solve it by using `conda install airflow`, but this is just for local development purposes.