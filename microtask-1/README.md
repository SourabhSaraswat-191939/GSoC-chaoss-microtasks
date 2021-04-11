## Microtask-1

Setting up a dev environment to work on GrimoireLab .

### Steps
1. Download and install PyCharm .
2. Then I Installed ElasticSearch(6.8.6), Kibiter(6.8.6) and MariaDB database using Docker-Compose (with SearchGuard) .
3. Cloned all GrimoireLab repos using this [Python Script](https://gist.github.com/vchrombie/4403193198cd79e7ee0079259311f6e8)

   Before running script I installed PyGitHub and GitPython modules in the virtualenvironment .
  
       $ python3 -m pip install PyGitHub GitPython
   
   After this running script using following command (Replace the xxxx with the GitHub API Token) :
       
       $ python3 glab-dev-env-setup.py -c -t xxxx
  
4. Installed the dependencies through Project Interpreter .
5. Added the forked github repository as dependencies to the grimoirelab components using Project Structure .
 

Screenshot after Project Setup in Pycharm with all dependencies and project configuration .

![Project_Setup](https://github.com/SourabhSaraswat-191939/GSoC-chaoss-microtasks/blob/main/microtask-1/Project_Setup.png)
