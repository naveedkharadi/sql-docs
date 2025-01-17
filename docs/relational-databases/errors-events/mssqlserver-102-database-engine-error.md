---
description: "MSSQLSERVER_102"
title: "MSSQLSERVER_102 | Microsoft Docs"
ms.custom: ""
ms.date: "04/04/2017"
ms.service: sql
ms.reviewer: ""
ms.subservice: supportability
ms.topic: "reference"
helpviewer_keywords: 
  - "102 (Database Engine error)"
ms.assetid: 264dc1a2-c8a0-4c89-b5f6-951baf950299
author: MashaMSFT
ms.author: mathoma
---
# MSSQLSERVER_102
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## Details  
  
| Attribute | Value |  
| :-------- | :---- |  
|Product Name|SQL Server|  
|Event ID|102|  
|Event Source|MSSQLSERVER|  
|Component|SQLEngine|  
|Symbolic Name|P_SYNTAXERR2|  
|Message Text|Incorrect syntax near '%.*ls'.|  
  
## Explanation  
Indicates a syntax error. Additional information is not available because the error prevents the [!INCLUDE[ssDE](../../includes/ssde-md.md)] from processing the statement.  
  
Can be caused by attempting to create a symmetric key using the deprecated RC4 or RC4_128 encryption, when not in 90 or 100 compatibility mode.  
  
## User Action  
Search the [!INCLUDE[tsql](../../includes/tsql-md.md)] statement for syntax errors.  
  
If creating a symmetric key using the RC4 or RC4_128, select a newer encryption such as one of the AES algorithms. (Recommended.) If you must use RC4, use ALTER DATABASE SET COMPATIBILITY_LEVEL to set the database to compatibility level 90 or 100. (Not recommended.)  
  
