# Setings

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
