# AIRFLOW + WSL

#### CASO NÃO TENHA WSL INSTALADO NA MÁQUINA

- wsl --install
- wsl -l -v

#### INSTALAR PYTHON E VENV

- sudo apt update
- sudo apt upgrade
- sudo add-apt-repository ppa:deadsnakes/ppa
- sudo apt install python3.9
- sudo apt install python3.9-venv
- supo apt install python3.9-pip

#### INSTALAR O AIRFOW

- source venv/bin/activate
- AIRFLOW_VERSION=2.3.2
- PYTHON_VERSION=3.9
- CONSTRAINT_URL="https://raw.githubusercontent.com/apache/airflow/constraints-${AIRFLOW_VERSION}/constraints-${PYTHON_VERSION}.txt"
- pip install "apache-airflow[postgres,celery,redis]==${AIRFLOW_VERSION}" --constraint "${CONSTRAINT_URL}"
- export AIRFLOW_HOME=$(pwd)/airflow_pipeline
- airflow standalone
