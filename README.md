# cryptoman
A public plugin for crypto payment over Kenar Divar platform

## Installation

- install [pyenv](https://github.com/pyenv/pyenv)
- install [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv)
- install [poetry](https://github.com/sdispater/poetry)
- install python 3.12.6 via pyenv

```bash
pyenv install 3.12.6
```

- create virtualenv

```bash
pyenv virtualenv 3.12.6 cryptoman_env_3.12.6
pyenv activate cryptoman_env_3.12.6
```

- set pyenv local version in the root folder

```bash
pyenv local cryptoman_env_3.12.6
```

- install dependencies

```bash
poetry install --no-dev
```


## Run Local

Setup a PosgreSQL and update environment parameters. The following command can set the sample env. file in the environment.

```bash
soure sample.env
```

Then run the project using poetry command. Before running the sever, migrate all models to database if it is the first time.
```bash
poetry run python manage.py migrate
```

```bash
poetry run python manage.py runserver
```
