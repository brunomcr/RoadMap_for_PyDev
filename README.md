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

<hr>

<details>
  <summary>
    <h3>Windows</h3>
  </summary> 
  
  #### CMD
  * `echo "text_to_print"` - Write in the console
  * `echo "text_to_print" > <fileName>` - ">" Create a fileName to write the content.
  * `echo "text_to_print" >> <fileName>` - ">>"  Create if not ecxist or open a fileName to write the content.
  * `@echo off` - Makes the commands that are in the scripts not appear during their execution, showing only their results.
  * `DIR` - List the folders and files in the current directory.
  * `mkdir` - Make a directory.
  * `rmdir` - Remove a directory.
  * `CD` - Change Directory.
    * `CD <dirName>`
    * `CD ..`
  * `move <fileName> <pathToMove>` - Move file to other location.
  * `type <fileName>` - Read and return its content in the console.
  * `more <fileName>` - Read and return its content in the console.
  * `copy <fileName> <fileNewName>` - Copy a file with new name.
  * `xcopy <dirName> <dirNewName>` - Copy a dir with new name.
  * `rename <fileName> <fileNewName>` - Rename the file.
  * `del <fileName>` - Delete file.
  * `cls` - Clear Screen.
  * `tree` - Shows folders and subfolders arranged in a tree.
  * `pause` - Waits for a user interaction with the terminal.
  * `PATH` - Variable where paths to scripts are found
  * `set` - Set a temporary variable, while cmd is open.
  * `setx` - Set a permanentely variable.
    * `setx <VAR_NAME>=<VAR_VALUE> /M`
    
  
    
  #### Windows Security Authorization
  ```
    Get-ExecutionPolicy
  ```
  ```
    Set-ExecutionPolicy Unrestricted -Scope Process
  ```
  ```
    Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted
  ```
</details>  

<hr>

<details>
  <summary>
    <h3>Python</h3>
  </summary>
  
</details>

<hr>

<details>
  <summary>
    <h3>Black</h3>
  </summary>
  
</details>

<hr>

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

<hr>
  
<details>
  <summary>
    <h3>Virtual Env (W,Windows),(L,Linux),(M,Mac)</h3>
  </summary> 

  #### Create virtual environment (W,L)
  * virtualenv: ```virtualenv <envName>```
  * python3 venv: ```python3 -m venv <envName>```

  #### Start virtual environment 
  * (W): ```.\\<patchEnv>\<envName>\Scripts\activate```
  * (L): ```source <patchEnv>/<envName>/bin/activate```

  #### Stop virtual environment (W,L)
  ```deactivate```
</details>

<hr>
  
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
  #### Run
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

<hr>

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

<hr>

<details>
  <summary>
    <h3>PostgreSQL</h3>
  </summary>
</details>

<hr>

<details>
  <summary>
    <h3>Pytest</h3>
  </summary>

  ### Settings:
  #### pyproject.toml
  ```
  [tool.pytest.ini_options]<br>
  python_files = ["test_*.py", "*_test.py"]<br>
  DJANGO_SETTINGS_MODULE = "<djangoProject>.settings"
  ```

  ### How to use
  * ```@pytest.fixture```: Is a function that's run every time is called.
  * ```@pytest.mark.django_db```: Database access for test function.

  Pattern for writing tests:
  * Arrange
  * Act
  * Assert

  Capture stdout
  ```
  pytest -s
  ```
  * ```pytest -rP```: for captured output of passed tests
  * ```pytest -rx```: for captured output of failed tests (default behaviour).
</details>

<hr>

<details>
  <summary>
    <h3>Factory Boy</h3>
  </summary>

  * Returns a User instance that's not saved:
    * ```user = UserFactory.build()```

  * Returns a saved User instance.
    * UserFactory must subclass an ORM base class, such as DjangoModelFactory.
    * ```user = UserFactory.create()```

  * Returns a stub object (just a bunch of attributes)
    * ```obj = UserFactory.stub()```
</details>

<hr>
  
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

<hr>

<details>
  <summary>
    <h3>Docker Compose</h3>
  </summary>

  #### Build
  ```
  docker-compose up --build
  ```
</details>

<hr>

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
  Use the ```git remote -v``` command to confirm that a remote named heroku has been set for your app
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
