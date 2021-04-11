## Microtask-2

Executing micro-mordred to collect, enrich and visualizing data from Git repositories.

### Steps 

1. Before Executing micro-mordred firstly run the following command where your docker-compose.yml is present :
          
          docker-compose up 
   This will start Kibiter ,MariaDB and ElasticSearch.

2. Then I defined my tokens in setup.cfg and changed projects.json to list of project which data I want .
3. Created a configuration in PyCharm to speed up the executions of micro-mordred .
   
   Screenshot after creating Configuration :
   ![after_creating_Conf](https://github.com/SourabhSaraswat-191939/GSoC-chaoss-microtasks/blob/main/microtask-2/after_creating_Conf.png)
   
4. Executed micro-mordred , but I received an error :
   
   :x: "This error was of connection with database of docker. '" :x:
   
   I solved this issue by changing Mariadb configuration of docker-compose(with SearchGuard) and I also generated a PR for this.
   
   Detailed issue and solution is mentioned in my PR [#501](https://github.com/chaoss/grimoirelab-sirmordred/pull/501) ✔️
   
   After solving this, I Executed micro-mordred .
   
Screenshot of Executing micro-mordred to collect data from Git repositories :

![Run Micro Mordred](https://github.com/SourabhSaraswat-191939/GSoC-chaoss-microtasks/blob/main/microtask-2/Run_Micro_Mordred.png)

Now after that, Screenshot of visualizing data from Git repositories using Kibiter :

![Git Visualization Kibiter](https://github.com/SourabhSaraswat-191939/GSoC-chaoss-microtasks/blob/main/microtask-2/Git_visualization_Kibiter.png)
