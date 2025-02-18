---
description: "updateBytes Method (SQLServerResultSet)"
title: "updateBytes Method (SQLServerResultSet) | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2017"
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ""
ms.technology: connectivity
ms.topic: reference
apiname: 
  - "SQLServerResultSet.updateBytes"
apilocation: 
  - "sqljdbc.jar"
apitype: "Assembly"
ms.assetid: 3050c836-fbb3-4475-99e5-05637a48a932
author: David-Engel
ms.author: v-davidengel
---
# updateBytes Method (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Updates the designated column with an array of **byte** values.  
  
## Overload List  
  
|Name|Description|  
|----------|-----------------|  
|[updateBytes (int, byte&#91;&#93;)](../../../connect/jdbc/reference/updatebytes-method-int-byte.md)|Updates the designated column with an array of **byte** values given the column index.|  
|[updateBytes (java.lang.String, byte&#91;&#93;)](../../../connect/jdbc/reference/updatebytes-method-java-lang-string-byte.md)|Updates the designated column with an array of **byte** values given the column name.|  
  
## Remarks  
 In a previous version of [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)], you could use SQLServerResultSet.updateBytes to convert values between byte arrays and [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] data type **date**, **time**, **datetime2**, or **datetimeoffset**. Now, using this method with those data types will cause an exception indicating that the conversion is not supported.  
  
## See Also  
 [SQLServerResultSet Members](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet Class](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
