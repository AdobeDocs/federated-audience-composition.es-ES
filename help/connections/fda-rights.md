---
title: Permisos para acceder a una base de datos externa
description: Obtenga información sobre los derechos específicos de cada motor de base de datos
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 46%

---

# Matriz de derechos de FDA {#fda-rights}

La siguiente tabla describe los privilegios de base de datos necesarios para cada sistema, lo que permite a los usuarios realizar operaciones en bases de datos externas a través de FDA.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Conexión a la base de datos remota** | USO EN ALMACÉN (WAREHOUSE), USO EN BASE DE DATOS (DATABASE ) y USO EN PRIVILEGIOS DE ESQUEMA (SCHEMA) | Creación de un usuario vinculado a la cuenta de AWS | Crear una cuenta de servicio y conceder acceso principal al proyecto | Privilegio USE CATALOG en el catálogo y privilegio CAN_USE en el almacén SQL |
| **Creación de tablas** | Privilegio CREATE TABLE ON SCHEMA | Privilegio CREATE | La función asignada a la cuenta de servicio debe contener los permisos bigquery.jobs.create y bigquery.tables.create | Privilegio USE SCHEMA y privilegio CREATE TABLE |
| **Creación de índices** | N/A | Privilegio CREATE | BigQuery solo admite índices de búsqueda. La función asignada a la cuenta de servicio debe contener los permisos bigquery.jobs.create, bigquery.tables.getData y bigquery.tables.createIndex | N/A |
| **Creación de funciones** | Privilegio CREATE FUNCTION ON SCHEMA | El privilegio USAGE ON LANGUAGE plpythonu podrá llamar scripts de python externos | La función asignada a la cuenta de servicio debe contener los permisos bigquery.jobs.create y bigquery.routines.create | Privilegio CREATE FUNCTION |
| **Creación de procedimientos** | N/A | El privilegio USAGE ON LANGUAGE plpythonu podrá llamar scripts de python externos | La función asignada a la cuenta de servicio debe contener los permisos bigquery.jobs.create y bigquery.routines.create |  N/D |
| **Eliminación de objetos (tablas, índices, funciones, procedimientos)** | Propiedad del objeto | Tener el objeto o ser un superusuario | La función asignada a la cuenta de servicio debe contener los permisos bigquery.jobs.create, bigquery.routines.delete, bigquery.tables.delete y bigquery.tables.deleteIndex |
| **Monitoreo de las ejecuciones** | Privilegio MONITOR en el objeto requerido | No se requiere ningún privilegio para utilizar el comando EXPLAIN | función monitoring.viewer | Privilegio CAN_VIEW |
| **Escritura de datos** | Privilegios INSERT o UPDATE (según la operación de escritura) | Privilegios INSERT y UPDATE | La función asignada a la cuenta de servicio debe contener: bigquery.jobs.create y bigquery.tables.updateData |  Privilegio MODIFY |
| **Carga de datos en tablas** | Privilegios CREATE STAGE ON SCHEMA, SELECT e INSERT en la tabla de destino | Privilegios SELECT e INSERT | La función asignada a la cuenta de servicio debe contener: bigquery.jobs.create, bigquery.tables.getData y bigquery.tables.updateData | Privilegios SELECT y MODIFY |
| **Acceso a los datos del cliente** | Privilegios SELECT en (FUTURE) TABLE(S) o VIEW(S) | Privilegio SELECT | La función asignada a la cuenta de servicio debe contener: bigquery.jobs.create y bigquery.tables.getData para tablas o la función bigquery.dataViewer |  Privilegio SELECT |
| **Acceso a metadatos** | Privilegio SELECT en INFORMATION_SCHEMA SCHEMA | Privilegio SELECT | función bigquery.metadataViewer |  Privilegio SELECT en INFORMATION_SCHEMA SCHEMA |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Conexión a la base de datos remota** | Permiso Leer (predeterminado) | Permiso CONNECT | No se requiere ningún privilegio. |
| **Creación de tablas** | CREATE TABLE ON DATABASE (almacén) y ALTER ON SCHEMA | Permiso CREATE TABLE | Privilegio CREATE ON SCHEMA |
| **Creación de índices** | N/A | Permiso ALTER | N/A |
| **Creación de funciones** | N/A | Permiso CREATE FUNCTION | Privilegio CREATE ON SCHEMA |
| **Creación de procedimientos** | CREATE PROCEDURE ON DATABASE (almacén) y ALTER ON SCHEMA | Permiso CREATE PROCEDURE | Privilegio CREATE ON SCHEMA |
| **Eliminación de objetos (tablas, índices, funciones, procedimientos)** | ALTERAR EN EL ESQUEMA | Permiso ALTER | ser propietario del objeto o del privilegio DROP en el objeto |
| **Monitoreo de las ejecuciones** | Permisos de colaborador de Workspace o superiores (queryinsights.exec_requests_history)  | Permiso CONTROL | No se requiere ningún privilegio para utilizar la instrucción EXPLAIN |
| **Escritura de datos** | INSERTAR y/o ACTUALIZAR EN OBJETO | Permisos INSERT y UPDATE | Privilegios INSERT y UPDATE |
| **Carga de datos en tablas** | SELECCIONAR EN OBJETO e INSERTAR EN OBJETO | Permisos CREATE TABLE, EXECUTE, SELECT, INSERT, UPDATE, ALTER | Privilegio INSERT en tabla, privilegio USAGE en esquema |
| **Acceso a los datos del cliente** | SELECCIONAR EN OBJETO | Permiso SELECT | Privilegio SELECT |
| **Acceso a metadatos** | SELECCIONAR EN INFORMATION_SCHEMA | No se requiere permiso para describir la tabla | USAGE ON SCHEMA, SELECT en TABLE y también privilegios en las tablas v_catalog.columns y v_catalog.view_columns |
