## Linux
#### Kill process in specif PORT:
* `sudo kill -9 $(sudo lsof -t -i:8000)`


## Git
#### Status
* `git status`
#### Init
* `git init`
#### Checkout for a new branch
* `git checkout -b "<branchName>"`
#### Others Command
* `git add <projectName>` or `git add .`
* `git commit -m "<Commit Menssage>"`
* `git remote add origin <SSHpatchGit>`
* `git pull origin main --allow-unrelated-histries`
* `git push`
* `git log`


## Poetry
#### New Project (will create a python project)
* `poetry new <projectName>`
#### New Init (will create a pyproject.toml)
* `poetry init`
#### Start a virtuenv
* `source $(poetry env info --path)/bin/activate`
#### Build
* `poetry build`
#### Publish
* `poetry publish`
#### Export Requirements
* `poetry export -o <fileName>.txt`
#### Install Package
* `poetry add <namePackage>`


### Poetry + Django
* `poetry run`+`<django command>`
  #### Start a Django Project
  * `poetry run` `django-admin startproject <projectName>`
  #### Start a Django App
  * `poetry run` `py manage.py startapp <appName>`


## Djando
#### Create Project
* `django-admin startproject <projectName>`
* `django-admin startproject <projectName> .` (create project, without create a new dir) 

#### Create App
* `python manage.py startapp <appName>`

#### Install App
* open Settings.py and add you `<appName>` to list `INSTALLED_APPS`

#### Migrate / Makemigrations
* `python manage.py migrate`
* `python manage.py makemigrations`

#### Run Server
* `python manage.py runserver`

#### Create Super User (Admin)
* `python manage.py createsuperuser`


## PostgreSQL


## Docker
#### Build
* `docker build`
  * `docker build --tag <imageName> .`  
* Run
* `docker run --name <imageName> -d -p <localPort>:<dockerPort> <imageName>:<versionTag>`
  * Exemple: `docker run --name bookstore -d -p 8000:8000 bookstore:latest`
#### Publish
* `docker push` 
#### Info.
* `docker images`
* `docker ps` and `docker ps -a`
