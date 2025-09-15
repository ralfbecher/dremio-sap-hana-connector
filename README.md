# Dremio SAP HANA ARP  Connector
<img src="./src/main/resources/SAPHANA.svg" width="180">

## Overview
This is a community based SAP HANA Dremio connector made using the ARP framework. Check [Dremio Hub](https://github.com/dremio-hub) for more examples and [ARP Docs](https://github.com/dremio-hub/dremio-sqllite-connector#arp-file-format) for documentation.

## What is Dremio?

Dremio delivers lightning fast query speed and a self-service semantic layer operating directly against your data lake storage and other sources. No moving data to proprietary data warehouses or creating cubes, aggregation tables and BI extracts. Just flexibility and control for Data Architects, and self-service for Data Consumers.

## Usage


### Required Parameters

- SAP HANA URL
- USER NAME
- PASSWORD

## Development

## Building and Installation

0. Change the pom's dremio.version to suit your Dremio's version.
   `<version.dremio>25.2.0-202410241428100111-a963b970</version.dremio>`
1. In root directory with the pom.xml file run `mvn clean install -DskipTests`. If you want to run the tests, add the JDBC jar to your local maven repo along with environment variables that are required. Check the basic test example for more details.
1. Take the resulting .jar file from the target folder and put it in the <DREMIO_HOME>\jars folder in Dremio
2. Download the SAPA HANA JDBC driver from ([repo](https://mvnrepository.com/artifact/com.sap.cloud.db.jdbc/ngdbc)) and put in in the <DREMIO_HOME>\jars\3rdparty folder
3. Restart Dremio

## Changes

- Updated for Dremio version 25.2.0
- Updated repository URLs from HTTP to HTTPS in pom.xml
- Fixed CredentialsService import path
