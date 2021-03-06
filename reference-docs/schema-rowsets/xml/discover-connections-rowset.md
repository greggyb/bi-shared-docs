---
title: "DISCOVER_CONNECTIONS Rowset | Microsoft Docs"
ms.date: 07/25/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: schema-rowsets
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
---
# DISCOVER_CONNECTIONS Rowset

  Provides resource usage and activity information about the currently opened connections on the server.  
  
 **Applies to:** tabular models, multidimensional models  
  
## Rowset Columns  
 The **DISCOVER_CONNECTIONS** rowset contains the following columns.  
  
|Column name|Type indicator|Restrictions|Description|  
|-----------------|--------------------|------------------|-----------------|  
|**CONNECTION_ID**|**DBTYPE_I4**|Yes|A unique number that identifies the connection.|  
|**CONNECTION_USER_NAME**|**DBTYPE_WSTR**|Yes|The connection user name.|  
|**CONNECTION_IMPERSONATED_USER_NAME**|**DBTYPE_WSTR**|Yes|Reserved for future use. Analysis Services always returns NULL for the value of CONNECTION_IMPERSONATED_USER_NAME.|  
|**CONNECTION_HOST_NAME**|**DBTYPE_WSTR**|Yes|The name of the machine that initiated the connection.|  
|**CONNECTION_HOST_APPLICATION**|**DBTYPE_WSTR**||The name of the application that initiated the connection.|  
|**CONNECTION_START_TIME**|**DBTYPE_DBTIMESTAMP**||The server UTC date and time when the connection was initiated.|  
|**CONNECTION_ELAPSED_TIME_MS**|**DBTYPE_I8**|Yes|Elapsed time, in milliseconds, since the start of the connection.|  
|**CONNECTION_LAST_COMMAND_START_TIME**|**DBTYPE_DBTIMESTAMP**||The server UTC date and time when the last command initiated its execution.|  
|**CONNECTION_LAST_COMMAND_END_TIME**|**DBTYPE_DBTIMESTAMP**||The server UTC date and time when the last command finished its execution.|  
|**CONNECTION_LAST_COMMAND_ELAPSED_TIME_MS**|**DBTYPE_I8**|Yes|The elapsed time, in milliseconds, since the end of the last command executed.|  
|**CONNECTION_IDLE_TIME_MS**|**DBTYPE_I8**|Yes|The idle time, in milliseconds, since the start of the connection.|  
|**CONNECTION_BYTES_SENT**|**DBTYPE_I8**||The accumulated number of bytes sent by the connection since the start of the connection.|  
|**CONNECTION_DATA_BYTES_SENT**|**DBTYPE_I8**||The accumulated number of data bytes sent by the connection since the start of the connection.<br /><br /> Data travels compressed within the connection; this value represents the expanded data sent.|  
|**CONNECTION_BYTES_RECEIVED**|**DBTYPE_I8**||The accumulated number of bytes received by the connection since the start of the connection.|  
|**CONNECTION_DATA_BYTES_RECEIVED**|**DBTYPE_I8**||The accumulated number of data bytes received by the connection since the start of the connection.<br /><br /> Data travels compressed within the connection; this value represents the expanded data received.|  
  
 This schema rowset is not sorted.  
  
## Using ADOMD.NET to return the rowset  
 When using ADOMD.NET and the schema rowset to retrieve metadata, you can use either the GUID or string to reference a schema rowset object in the GetSchemaDataSet method.
  
 The following table provides the GUID and string values that identify this rowset.  
  
|Argument|Value|  
|--------------|-----------|  
|GUID|a07ccd25-8148-11d0-87bb-00c04fc33942|  
|ADOMDNAME|Connections|  
