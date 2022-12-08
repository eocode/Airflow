<div align="center">
  <div align="center">
      <img width="200px" src="./airflow.png" 
      alt="Roomer"/>
  </div>
  <p align="center">
    <a href="https://github.com/eocode/Cerebro-Bot/blob/master/LICENSE" target="__blank">
      	<img src="https://img.shields.io/badge/License-GPLV3-blue.svg"  alt="license badge"/>
    </a>
    <a href="https://github.com/ambv/black" target="__blank">
        <img src="https://img.shields.io/badge/code%20style-black-000000.svg" />
    </a>
  </p>
</div>

Create VENV

```cmd
python -m venv env
```

```cmd
# .env file
AIRFLOW_UID=1000
AIRFLOW_GID=0
```

Install airflow

```cmd
pip install "apache-airflow[celery]==2.4.3" --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.4.3/constraints-3.7.txt"
```

Manage commands

```cmd
docker exec -it airflow_airflow-worker_1 bash
```

```cmd
./airflow.sh bash
```

```cmd
./airflow.sh info
```

```cmd
./airflow.sh python
```

Test a task
```cmd
airflow tasks test process_user create_table 2022-11-29
```

Configurations

airflow.cfg

```
airflow config get-value core sql_alchemy
```

```
airflow config get-value core executor
```