---
description: "getTrustManagerClass Method (SQLServerDataSource)"
title: "getTrustManagerClass Method (SQLServerDataSource) | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ""
ms.technology: connectivity
ms.topic: reference
apiname: 
  - "SQLServerDataSource.getTrustManagerClass"
apilocation: 
  - "sqljdbc.jar"
apitype: "Assembly"
ms.assetid:
author: David-Engel
ms.author: v-davidengel
---
# getTrustManagerClass Method (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Returns the String value of the TrustManagerClass connection property.
  
## Syntax  
  
```  
  
public java.lang.String getTrustManagerClass()  
```  
  
## Return Value  
 A **String** that contains the value of the TrustManagerClass connection property, or null if no value is set.  
  
## Remarks  
 If the TrustManagerClass property is not set, the [getTrustManagerClass](../../../connect/jdbc/reference/gettrustmanagerclass-method-sqlserverdatasource.md) method returns null.  
  
## See Also  
 [SQLServerDataSource Members](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource Class](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
