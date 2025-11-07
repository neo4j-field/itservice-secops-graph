# IT Service Graph demo with additional DevSecOps data

The Demo is using Neo4j and Neodash building an IT Service Graph UI that was exteded by a Security Operations Dashboard. The Demo was forked from this [repo](https://github.com/neo4j-field/itservicegraph) and extended with an additional SecOps Graph part (that also could stand on its own).

We added DevSecOps data to the original use case in order to show the power of knowledge graphs and its flexibility extending the data model with more "knowledge".

The vulnerability analysis has been done using SCA and SAST scanners. Anybody can replace the demo data with real SBOMs and reports from Trivy and Bearer.

The Demo is aimed to show a Knowledge Graph consisting of IT Infrastructure Data as well as IT Services and Customer Information. Adding Security and SBOM information helps people responsible for security to have 'actionable insights' to the complete service chain. They are able to view security related findings and the complete information from the software component, software, vulnerability, server up to the datacenter, the server is running and its rack position.
Such data comes from various data sources and provides deep actionable insides, that no one tool can provide.

## Screenshots

#### Overview - Showing number of applications, scanner tooling used, etc.
![Overview and DevSecOps adoption](
https://github.com/neo4j-field/itservice-secops-graph/blob/9d88ce17e6f336dfc06b9654aecd6114c77f5f68/graphics/secOps_Overview.png)

#### SCA drill down - Allows for drilling into applications and their vulnerabilities
![SCA drill down](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_sca-drill-down.png)

#### SCA overview - Vulerability information with clickable buttons to investigate into the software structure
![SCA overview](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_sca-overview.png)

#### SCA search - Allows to search for software-components and find vulnerable components found with additional information
![SCA search Tab](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_sca-search.png)

#### SAST overview - Allows to drill through SAST findings and details about the findings
![SAST Overview Tab](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_sast-overview.png)

#### Affected Servers/Customers - Can be used to search for findings to see the affected software, thus effected services with its complete service chain and customer details.
![Affected Servers/Customers Tab](https://github.com/neo4j-field/itservice-secops-graph/blob/4af41c86772f8b98e38d49a5576494520b304737/graphics/secOps_affected-customers.png)


## Demo Installation

**NOTE:** All server, customer and software data in the graph was syntetically generated, thus names, version, etc. do not exist in the real world and are only used for demo purpose. The SecOps data is REAL data linked to the artificial software and services. This may all be replaced with real information easily!

The installation of the IT Services Graph part of the demo, will not be described again. Please refer to the [original repo](https://github.com/neo4j-field/itservicegraph). Never the less, all data and dashboards can be found in this repo! Only use the load scripts and dashboard files from here! 

As mentioned, the installation of the demo is the same and was explained in the original repo. But in addition it is required to run more load scripts. Also import both, the IT Service and the SecOps dashboards (found in ```./neodash```) into Neodash to get the full view of all data. Please run the load scripts(found in ```./load```) in the order as they are named! Start with 1_... up to 4_...! That will guarantee, the data is complete and the knowledge graph is build up correctly. Then import the dashboard files into Neodash as described in the original gitrepo.

Have fun with the demo!
  
