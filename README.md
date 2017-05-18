# Simple standalone sitecore setup with docker
## Installation
clone the repo:

	git clone https://github.com/aserogin/simple-sitecore-docker.git

* [Download the Sitecore](https://dev.sitecore.net/Downloads/Sitecore_Experience_Platform/82/Sitecore_Experience_Platform_82_Update3.aspx)
* Unzip and copy the Sitecore files into the sitecore folder.
* Change sitecore/Website/App_Config/ConnectionString.config 
    - use "mongodb" as dns name for mongo
    - use "mssql" as dns name for Microsoft SQL Server
    - use sa/Q!w2e3r4t5 for SQL Server authentication
* Change path to data folder in sitecore/Website/App_Config/Include/DataFolder.config to following "C:/Workplace/Data/"
* Copy your license.xml into sitecore/Data

## Usage
Run docker-compose in your cli:

	docker-compose up