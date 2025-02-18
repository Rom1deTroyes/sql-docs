---
description: "sys.sequences (Transact-SQL)"
title: "sys.sequences (Transact-SQL) | Microsoft Docs"
ms.custom: ""
ms.date: "06/10/2016"
ms.prod: sql
ms.prod_service: "database-engine, sql-database"
ms.reviewer: ""
ms.technology: system-objects
ms.topic: "reference"
f1_keywords: 
  - "sys.sequences_TSQL"
  - "sys.sequences"
  - "sequences"
  - "sequences_TSQL"
dev_langs: 
  - "TSQL"
helpviewer_keywords: 
  - "sequence number object, sys. sequences catalog view"
  - "sys.sequences catalog view"
ms.assetid: 0e1b0e32-1cce-40f7-83c8-860ec660138a
author: rwestMSFT
ms.author: randolphwest
monikerRange: "=azuresqldb-current||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current"
---
# sys.sequences (Transact-SQL)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

  Contains a row for each sequence object in a database.  
  
|Column name|Data type|Description|  
|-----------------|---------------|-----------------|  
|\<inherited columns>||Inherits all columns from [sys.objects](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md).|  
|**start_value**|**sql_variant NOT NULL**|The starting value for the sequence object. If the sequence object is restarted by using ALTER SEQUENCE it will restart at this value. When the sequence object cycles it proceeds to the **minimum_value** or **maximum_value**, not the **start_value**.|  
|**increment**|**sql_variant NOT NULL**|The value that is used to increment the sequence object after each generated value.|  
|**minimum_value**|**sql_variant NULL**|The minimum value that can be generated by the sequence object. After this value is reached, the sequence object will either return an error when trying to generate more values or restart if the CYCLE option is specified. If no MINVALUE has been specified, this column returns the minimum value supported by the sequence generator's data type.|  
|**maximum_value**|**sql_variant NULL**|The maximum value that can be generated by the sequence object. After this value is reached the sequence object will either start returning an error when trying to generate more values or restart if the CYCLE option is specified. If no MAXVALUE has been specified this column returns the maximum value supported by the sequence object's data type.|  
|**is_cycling**|**bit NOT NULL**|Returns 0 if NO CYCLE has been specified for the sequence object and 1 if CYCLE has been specified.|  
|**is_cached**|**bit NOT NULL**|Returns 0 if NO CACHE has been specified for the sequence object and 1 if CACHE has been specified.|  
|**cache_size**|**int NULL**|Returns the specified cache size for the sequence object. This column contains NULL if the sequence was created with the NO CACHE option or if CACHE was specified without specifying a cache size. If the value specified by the cache size is larger than the maximum number of values that can be returned by the sequence object, that unobtainable cache size is still displayed.|  
|**system_type_id**|**tinyint NOT NULL**|ID of the system type for sequence object's data type.|  
|**user_type_id**|**int NOT NULL**|ID of the data type for the sequence object as defined by the user.|  
|**precision**|**tinyint NOT NULL**|Max precision of the data type.|  
|**scale**|**tinyint NOT NULL**|Max scale of the type. Scale is returned together with precision to give users complete metadata. Scale is always 0 for sequence objects because only integer types are allowed.|  
|**current_value**|**sql_variant NOT NULL**|The last value obligated. That is, the value returned from the most recent execution of the NEXT VALUE FOR function or the last value from executing the **sp_sequence_get_range** procedure. Returns the START WITH value if the sequence has never been used.|  
|**is_exhausted**|**bit NOT NULL**|0 indicates that more values can be generated from the sequence. 1 indicates that the sequence object has reached the MAXVALUE parameter and the sequence is not set to CYCLE. The NEXT VALUE FOR function returns an error until the sequence is restarted by using ALTER SEQUENCE.|  
|**last_used_value**|**sql_variant NULL**|Returns the last value generated by the [Next Value For](../../t-sql/functions/next-value-for-transact-sql.md) function. Applies to SQL Server 2017 and later.|  
  
## Permissions  
 In [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] and later versions, the visibility of the metadata in catalog views is limited to securables that a user either owns or on which the user has been granted some permission. For more information, see [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
## See Also  
 [Sequence Numbers](../../relational-databases/sequence-numbers/sequence-numbers.md)   
 [CREATE SEQUENCE &#40;Transact-SQL&#41;](../../t-sql/statements/create-sequence-transact-sql.md)   
 [ALTER SEQUENCE &#40;Transact-SQL&#41;](../../t-sql/statements/alter-sequence-transact-sql.md)   
 [DROP SEQUENCE &#40;Transact-SQL&#41;](../../t-sql/statements/drop-sequence-transact-sql.md)   
 [NEXT VALUE FOR &#40;Transact-SQL&#41;](../../t-sql/functions/next-value-for-transact-sql.md)   
 [sp_sequence_get_range &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-sequence-get-range-transact-sql.md)  
  
  
