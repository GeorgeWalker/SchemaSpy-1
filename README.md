# SchemaSpy
======================

Introduction
----------------

This project contains a Dockerfile and associated files that can be used to setup an automated database documentation tool.

It is compatible with environment variables common OpenShift application deployments.

SchemaSpy itself is an open source project located here:  http://schemaspy.sourceforge.net/

Installation
----------------

The application is meant to be installed as an OpenShift application using the Docker Strategy, by simply using this repo as the Git Repository for the new application.

You can also run it locally, if you have the following dependencies installed:

1) Node.js
2) Java (only JRE necessary; no java is compiled)
3) Graphviz

Run npm install to get the required Node.js dependencies, then npm start to run the server.  

Required Parameters
----------------
The environment must contain the following settings:

DATABASE_SERVICE_NAME - the hostname of the database server.  

POSTGRESQL_USER - username that will be used to connect to the database

POSTGRESQL_PASSWORD - password that will be used to connect to the database

POSTGRESQL_DATABASE - name of the database to connect to.

Normally these would be set by the OpenShift template used to deploy the application.

All database activity occurs on application startup, after which static content is served up on a basic HTTP server.
                  
Contribution
------------

Please report any [issues](https://github.com/bcgov/SchemaSpy/issues).

[Pull requests](https://github.com/bcgov/Swagger-Editor/pulls) are always welcome.

If you would like to contribute, please see our [contributing](CONTRIBUTING.md) guidelines.

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

License
-------

    Copyright 2016 Province of British Columbia

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at 

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

Maintenance
-----------

This repository is maintained by [BC Ministry of Transportation](http://www.th.gov.bc.ca/).
Click [here](https://github.com/orgs/bcgov/teams/tran/repositories) for a complete list of our repositories on GitHub.
