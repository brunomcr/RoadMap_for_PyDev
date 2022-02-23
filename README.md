# Setings

## Virtual Env (W,Windows),(L,Linux)
#### Create virtual environment (W,L)
* virtualenv: `virtualenv <envName>`
* python3 venv: `python3 -m venv <envName>`

#### Windows Security Authorization (W)
* `Set-ExecutionPolicy Unrestricted -Scope Process`

#### Start virtual environment 
* (W): `.\\<patchEnv>\<envName>\Scripts\activate`
* (L): `source <patchEnv>/<envName>/bin/activate`

#### Stop virtual environment (W,L)
* `deactivate`


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
* `poetry env use py`
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
  * `poetry run django-admin startproject <projectName>`
  #### Start a Django App
  * `poetry run py manage.py startapp <appName>`


## Djando
#### Create Project
* `django-admin startproject <projectName>`

#### Create App
* `python manage.py startapp <appName>`

#### Install App
* open Settings.py and add you `<appName>` to list `INSTALLED_APPS`

#### Migrate
* `python manage.py migrate`

#### Run Server
* `python manage.py runserver`

