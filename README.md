# IT Service Graph demo with additional DevSecOps data

The Demo is using Neo4j and NeoDash building an IT Service Graph UI that was exteded by a Security Operations Dashboard. The Demo was forked from this !(repo)[https://github.com/neo4j-field/itservicegraph] and extended with an additional SecOps Graph part (that also could stand on its own, but would be less valueable).

We added DevSecOps data to the original use case in order to show the power of knowledge graphs and its flexibility.

The vulnerability analysis has been done using SCA and SAST scanners. Anybody can replace the demo data with real SBOMs and reports from Trivy and Bearer.

The Demo is aimed to show a Knowledge Graph consisting of IT Infrastructure Data as well as IT Services and Customer Information. Adding security and sbom information it helps people responsible for security to have 'actionable insights'.

## Screenshots

#### Overall
![Overview and DevSecOps adoption](
https://github.com/neo4j-field/itservice-secops-graph/blob/9d88ce17e6f336dfc06b9654aecd6114c77f5f68/graphics/secOps_Overview.png)

#### SCA drill down
![SCA drill down](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_sca-drill-down.png)

#### SCA overview
![SCA overview](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_sca-overview.png)

#### SCA search
![SCA search Tab](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_sca-search.png)

#### SAST overview
![SAST Overview Tab](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_sast-overview.png)


#### Affected Servers/Customers
![Affected Servers/Customers Tab](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_affected-customers.png)


## Demo explanation

**NOTE:** All server, customer and software data in the graph was syntetically generated, thus names, version, etc. do not exist in the real world and are only used for demo purpose.

The explanation of the IT Services Graph part of the demo, will not be done again. It can be found at the original repo that is linked above. Never the less, both dashboards can be found in the ```./neodash``` directory of the repo.

The installation of the demo is the same, was explained in the original repo, but the addition of running more load scripts and also import the SecOps dashboard into Neodash.

It is recommended to import both Dashboards to have the full view of the complete data and demo!


In order to install the demo locally do the following:

1. Create an empty Neo4j database. Use for example [Neo4j Aura](https://console.neo4j.io/), an empty [Neo4j Sandbox](https://sandbox.neo4j.com/) or Neo4j Desktop.
2. Install the APOC plugin when you are running in Neo4J desktop
3. When the database is  up and running, open Neo4j Browser and run first the commands provided in the script ```indexes.cypher```
4. Next load the data and run the commands provided in the script ```load_all_it-service-data.cypher```
5. Once indexes/contraints are created, go to [NeoDash](https://neodash.graphapp.io/) if you are using AuraDB or a Sandbox and choose New Dashboard. Click "Yes" on the next dialog. In case you use Neo4j Desktop, make sure you installed NeoDash via the AppsGallery before you contiue.  
6. In the following dialog, enter the hostname (copy that from your AuraDB or Sandbox environments, if you use Neo4j Desktop run NeoDash locally and also choose "New Dashboard". But enter ```localhost``` as the connection string. Then click the ```Connect``` button (all types of Neo4j)
7. Once connected, click the ```+```icon in the upper right corner and choose ```Import```. In the window that opens, cut and paste the JSON content of the JSON file ```itgraph_dashboard_<last date saved>.json``` and paste it into the window. Scroll down and click the ```Import``` button to finally import the file. 
8. Then save it into your database by clicking the 3 dots on the left next to the braun rectangle with the name of the dashboard in it. It will become blue, once you confirm saving.
9. Enjoy the demo!  
