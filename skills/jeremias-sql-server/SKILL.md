---
name: jeremias-sql-server
description: Use this skill when asked to do actions related to SQL queries, related to Jeremias and the programs in use in our company
---

# General Information
- When using the connections in this file, make sure to always connect with Windows Authentication
- Always trust server certificate
- Don't use the _Test databases unless the user specifically asks for that

# MS-SQL Servers

## WT-S028\\SWPDM
Description: The main Server for all servers related to SE, meaning the custom programs developed by Jeremias, as well as hosting PDM databases

### Databases
- Laser
  - The database for everything related to our internal program "Laserpool"
- Laser_Test
  - Same as Laser but for tests
- Jeremias
  - The main production database for almost all our internal programs
  - Tables have no foreign keys and have been created with inconsistent normalisation
- Jeremias_Test
  - Same as Jeremias but for test
- PDM-Jeremias
  - The database for our main Solidworks PDM installation
  - Vaultname: "PDM Jeremias"
  - Use this as default for PDM requests
- SWPDM_PDMIndustriesArchiv
  - The database for our Solidworks PDM archive
  - Vaultname: "PDM Industries Archiv"
  - Use this if a request mentions the vaultname or archive in relation to PDM
- (LocalDb)\\MSSQLLocalDB
  - The database for our JeremiasPlatform project
  - Use this database exclusively for requests regarding the JeremiasPlatform project

## WT-S032\NAV
Description: The server that holds the Live data for our Microsoft Dynamics Navision installation

### Databases
- NAV_DE_2018_Live
  - The default database to use when the user requests Navision queries
  - By default use the "Jeremias GmbH$" tenant. Only use others when explicitly prompted by the user
  - Use this whenever the user wants data from the ERP software or Navision explicitly

## DC-S048\dynamics
Description: This server holds a variety of databases, along with the Navision test database and BC databases

### Databases
- NAV_DE_2018_Test
  - The default database to use when the user requests Navision test queries
  - By default use the "Jeremias GmbH$" tenant. Only use others when explicitly prompted by the user
  - Use this whenever the user wants test data from the ERP software or Navision explicitly
