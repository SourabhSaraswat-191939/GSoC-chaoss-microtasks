## Microtask-4

Set up the developer environment of SortingHat (muggle branch).

- Forked grimoirelab-sortinghat Repository .
- Clone the repositiry .
- Navigate to muggle branch using `git checkout muggle`.
- Install Poetry using command :
      
      curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
   
- Create a virtualenv using poetry by command : 

      poetry install
    
- Running virtualenv using poetry by command : 

      poetry shell
      
- Create a database in MySQL with name `sortinghat_db` .
- After this, moving on to next step I recieve an error 

    :x: "Error loading MySQLdb module: No module named 'MySQLdb'" :x:
 
 
   due to MySQLdb is only for Python 2.x .So to make it work for Python 3.x .
   
   So to solve as per [Stackoverflow](https://stackoverflow.com/questions/39574813/error-loading-mysqldb-module-no-module-named-mysqldb/39575675) .
   I added some set of line in `config/settings/init.py` . This __init__.py would be executed when we run the Django project, and MySQLdb will be replaced.
        
      import pymysql
      pymysql.version_info = (1, 4, 0, "final", 0)
      pymysql.install_as_MySQLdb()
   
- After this running commands for Migrations, fixtures and create a superuser :
      
      $ ./manage.py makemigrations --settings=config.settings.devel
      $ ./manage.py migrate --settings=config.settings.devel
      $ ./manage.py loaddata sortinghat/core/fixtures/countries.json --settings=config.settings.devel
      $ ./manage.py createsuperuser --settings=config.settings.devel
      
- Now, Running the backend using command :
      
      ./manage.py runserver --settings=config.settings.devel
      
#### Here is the Screenshot of backend server running:

![running_backend_sortinghat](https://github.com/SourabhSaraswat-191939/GSoC-chaoss-microtasks/blob/main/microtask-4/running_backend_sortinghat.png)

- Now, installing yarn using command :

        npm install -g yarn
   
- After this installing dependencies by using following command in `/ui` directory :

        yarn install
        
- Now Run SortingHat frontend Vue app UI using command :

        yarn serve


        
#### Here is the Screenshot of frontend server running:

![Running_frontend.png](https://github.com/SourabhSaraswat-191939/GSoC-chaoss-microtasks/blob/main/microtask-4/Running_frontend.png)
  
