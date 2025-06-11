---
title: Permisos para acceder a una base de datos externa
description: Obtenga información sobre los permisos que necesita para acceder y realizar tareas en cada motor de base de datos
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: 530a8709a67fabec1a36e1661b922f3e9a9e6996
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 25%

---

# Matriz de derechos de acceso a datos federados (FDA) {#fda-rights}

En la tabla siguiente se describen los permisos de base de datos necesarios para cada sistema, lo que permite realizar operaciones en bases de datos externas mediante el acceso de datos federado (FDA).

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Conexión a la base de datos remota** | Privilegios `USAGE ON WAREHOUSE`, `USAGE ON DATABASE` y `USAGE ON SCHEMA` | Crear un usuario vinculado a la cuenta de AWS | Crear una cuenta de servicio y conceder acceso principal al proyecto | Permiso `USE CATALOG` en el catálogo y permiso `CAN_USE` en el almacén SQL |
| **Creación de tablas** | Privilegio `CREATE TABLE ON SCHEMA` | Permiso `CREATE` | La función asignada a la cuenta de servicio debe contener: `bigquery.jobs.create` y `bigquery.tables.create` permisos | Permisos de `USE SCHEMA` y `CREATE TABLE` |
| **Creación de índices** | N/A | Permiso `CREATE` | BigQuery solo admite índices de búsqueda. La función asignada a la cuenta de servicio debe contener: `bigquery.jobs.create`, `bigquery.tables.getData` y `bigquery.tables.createIndex` permisos | N/A |
| **Creación de funciones** | Privilegio `CREATE FUNCTION ON SCHEMA` | Permiso `USAGE ON LANGUAGE plpythonu` para poder llamar scripts de Python externos | La función asignada a la cuenta de servicio debe contener: `bigquery.jobs.create` y `bigquery.routines.create` permisos | Permiso `CREATE FUNCTION` |
| **Creación de procedimientos** | N/A | Permiso `USAGE ON LANGUAGE plpythonu` para poder llamar scripts de Python externos | La función asignada a la cuenta de servicio debe contener: `bigquery.jobs.create` y `bigquery.routines.create` permisos |  N/D |
| **Eliminación de objetos (tablas, índices, funciones, procedimientos)** | Propiedad del objeto | Tener el objeto o ser un superusuario | La función asignada a la cuenta de servicio debe contener: `bigquery.jobs.create`, `bigquery.routines.delete`, `bigquery.tables.delete` y `bigquery.tables.deleteIndex` permisos | N/A |
| **Monitoreo de las ejecuciones** | Privilegio `MONITOR` en el objeto requerido | No se requieren permisos para utilizar el comando `EXPLAIN` | `monitoring.viewer` rol | Permiso `CAN_VIEW` |
| **Escritura de datos** | Privilegios `INSERT` o `UPDATE` (según la operación de escritura) | Permisos de `INSERT` y `UPDATE` | La función asignada a la cuenta de servicio debe contener: `bigquery.jobs.create` y `bigquery.tables.updateData` | Permiso `MODIFY` |
| **Carga de datos en tablas** | Privilegios de `CREATE STAGE ON SCHEMA`, `SELECT` y `INSERT` en la tabla de destino | Permisos de `SELECT` y `INSERT` | La función asignada a la cuenta de servicio debe contener: `bigquery.jobs.create`, `bigquery.tables.getData` y `bigquery.tables.updateData` | Permisos de `SELECT` y `MODIFY` |
| **Acceso a los datos del cliente** | Privilegios `SELECT on (FUTURE) TABLE(S)` o `VIEW(S)` | Permiso `SELECT` | La función asignada a la cuenta de servicio debe contener: `bigquery.jobs.create` y `bigquery.tables.getData` para las tablas o la función `bigquery.dataViewer` | Permiso `SELECT` |
| **Acceso a metadatos** | Privilegio `SELECT on INFORMATION_SCHEMA SCHEMA` | Permiso `SELECT` | `bigquery.metadataViewer` rol |  Permiso `SELECT on INFORMATION_SCHEMA SCHEMA` |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Conexión a la base de datos remota** | Permiso Leer (predeterminado) | Permiso `CONNECT` | No se requiere ningún privilegio. |
| **Creación de tablas** | `CREATE TABLE ON DATABASE` (almacén) y `ALTER ON SCHEMA` | Permiso `CREATE TABLE` | Privilegio `CREATE ON SCHEMA` |
| **Creación de índices** | N/A | Permiso `ALTER` | N/A |
| **Creación de funciones** | N/A | Permiso `CREATE FUNCTION` | Privilegio `CREATE ON SCHEMA` |
| **Creación de procedimientos** | `CREATE PROCEDURE ON DATABASE` (almacén) y `ALTER ON SCHEMA` | Permiso `CREATE PROCEDURE` | Privilegio `CREATE ON SCHEMA` |
| **Eliminación de objetos (tablas, índices, funciones, procedimientos)** | `ALTER ON SCHEMA` | Permiso `ALTER` | Propiedad del objeto o del privilegio `DROP` en el objeto |
| **Monitoreo de las ejecuciones** | Permisos de colaborador de Workspace o superiores (`queryinsights.exec_requests_history`) | Permiso `CONTROL` | No se requiere ningún privilegio para utilizar la instrucción `EXPLAIN` |
| **Escritura de datos** | `INSERT` o `UPDATE ON OBJECT` | Permisos de `INSERT` y `UPDATE` | Privilegios `INSERT` y `UPDATE` |
| **Carga de datos en tablas** | `SELECT ON OBJECT` y `INSERT ON OBJECT` | Permisos de `CREATE TABLE`, `EXECUTE`, `SELECT`, `INSERT`, `UPDATE` y `ALTER` | Privilegio `INSERT` en tabla, privilegio `USAGE` en esquema |
| **Acceso a los datos del cliente** | `SELECT ON OBJECT` | Permiso `SELECT` | Privilegio `SELECT` |
| **Acceso a metadatos** | `SELECT ON INFORMATION_SCHEMA` | No se requiere permiso para describir la tabla | `USAGE ON SCHEMA`, `SELECT on TABLE` y también privilegios en las tablas `v_catalog.columns` y `v_catalog.view_columns` |
