# WebDevOps a command-line guided RoadMap.
* Help command for creating a Web application and automating its integration and deployment.

## Linux (Ubuntu)
#### Kill process in specif PORT:
* `sudo kill -9 $(sudo lsof -t -i:8000)`

## Python

## Black (Optional)

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
### 
* `git remote -v`


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

#### Shell
* `python manage.py shell`


## PostgreSQL


## Docker
#### Build
* `docker build`
  * `docker build --tag <imageName> .`  
  * `docker build -t <imageName>:<versionTag> .`  
#### Run
* `docker run --name <imageName> -d -p <localPort>:<dockerPort> <imageName>:<versionTag>`
#### Publish
* `docker push` 
#### Info.
* `docker images`
* `docker ps` and `docker ps -a`
#### Delete images and containers
* `docker system prune`
#### Network
* `docker network ls`  


## Docker Compose
#### Build
* `docker-compose up --build`  


## Heroku
#### Login
* `heroku login`
### Create new App
* `heroku create -a <example-app>`
  * Use the `git remote -v` command to confirm that a remote named heroku has been set for your app:
#### Secrets Key / Authentication 
* `heroku auth:token`
#### Logs
* `heroku logs`
