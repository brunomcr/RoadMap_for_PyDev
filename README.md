# WebDevOps a command-line guided RoadMap.
* Help command for creating a Web application and automating its integration and deployment.


<details>
  <summary>
    <h3>Linux (Ubuntu)</h3>
  </summary> 
  
  #### Kill process in specif PORT:  
  ```
  sudo kill -9 $(sudo lsof -t -i:8000)
  ```  
</details>


<details>
  <summary>
    <h3>Python</h3>
  </summary>
  
</details>


<details>
  <summary>
    <h3>Black</h3>
  </summary>
  
</details>


<details>
  <summary>
    <h3>Git</h3>
  </summary>
  
  #### Status
  ```
  git status
  ```
  #### Init
  ```
  git init
  ```
  #### Checkout for a new branch
  ```
  git checkout -b "<branchName>"
  ```
  #### Others Command
  ```
  git add <fileName>` or `git add .
  ```  
  ```
  git commit -m "<Commit Menssage>"
  ```
  ```
  git remote add origin <SSHpatchGit>
  ```  
  ```
  git pull origin main --allow-unrelated-histries
  ```  
  ```
  git push
  ```  
  ```
  git log
  ```  
  ```
  git remote -v
  ```
</details>


<details>
  <summary>
    <h3>Poetry</h3>
  </summary>
  
  #### New Project (will create a python project)
  ```
  poetry new <projectName>
  ```
  #### New Init (will create a pyproject.toml)
  ```
  poetry init
  ```
  #### Start a virtuenv
  ```
  source $(poetry env info --path)/bin/activate
  ```
  #### Build
  ```
  poetry build
  ```
  #### Publish
  ```
  poetry publish
  ```
  #### Export Requirements
  ```
  poetry export -o <fileName>.txt
  ```
  #### Install Package
  ```
  poetry add <namePackage>
  ```
</details>


<details>
  <summary>
    <h3> Poetry + Django</h3>
  </summary>
  

  ```
  poetry run`+`<django command>
  ```
  #### Start a Django Project
  ```
  poetry run` `django-admin startproject <projectName>
  ```
  #### Start a Django App
  ```
  poetry run` `py manage.py startapp <appName>
  ```
</details>


<details>
  <summary>
    <h3>Djando</h3>
  </summary>
  

#### Create Project
```
django-admin startproject <projectName>
```
#### (create project, without create a new dir) 
```
django-admin startproject <projectName> .
``` 

#### Create App
```
python manage.py startapp <appName>
```

#### Install App
* open Settings.py and add you `<appName>` to list `INSTALLED_APPS`

#### Migrate / Makemigrations
```
python manage.py migrate
```
```
python manage.py makemigrations
```

#### Run Server
```
python manage.py runserver
```

#### Create Super User (Admin)
```
python manage.py createsuperuser
```

#### Shell
```
python manage.py shell
```
</details>


<details>
  <summary>
    <h3>PostgreSQL</h3>
  </summary>
  
 
</details>


<details>
  <summary>
    <h3>Docker</h3>
  </summary>

  #### Build
  ```
  docker build
  ```
  ```
  docker build --tag <imageName> .
  ```
  ```
  docker build -t <imageName>:<versionTag> .
  ```
  #### Run
  ```
  docker run --name <imageName> -d -p <localPort>:<dockerPort> <imageName>:<versionTag>
  ```
  #### Publish
  ```
  docker push
  ```
  #### Info.
  ```
  docker images
  ```
  ```
  docker ps` and `docker ps -a
  ```
  #### Delete images and containers
  ```
  docker system prune
  ```
  #### Network
  ```
  docker network ls
  ```
</details>


<details>
  <summary>
    <h3>Docker Compose</h3>
  </summary>

  #### Build
  ```
  docker-compose up --build
  ```
  </details>


  <details>
    <summary>
      <h3>Heroku</h3>
    </summary>


  #### Login
  ```
  heroku login
  ```
  #### Create new App
  ```
  heroku create -a <example-app>
  ```
    * Use the ```git remote -v``` command to confirm that a remote named heroku has been set for your app:
  #### Existing App
  ```
  heroku git:remote -a example-app
  ```
  #### Deploy Your Code
  ```
  git push heroku main
  ```
  #### Deploy From a Branch Besides main
  ```
  git push heroku testbranch:main
  ```
  #### Secrets Key / Authentication 
  * HEROKU_API_KEY ```heroku auth:token```
  #### Logs
  ```
  heroku logs
  ```
  ```
  heroku logs -t
  ```
  #### Stop Dynos process/session
  ```
  heroku ps:stop run.4859
  ```
</details>
