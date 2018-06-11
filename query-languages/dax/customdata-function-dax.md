---
title: "CUSTOMDATA Function (DAX) | Microsoft Docs"
ms.prod: dax
ms.date: 5/22/2018
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# CUSTOMDATA Function (DAX)
Returns the content of the **CustomData** property in the connection string.  
  
## Syntax  
  
```  
CUSTOMDATA()  
```  
  
## Return Value  
The content of the **CustomData** property in the connection string.  
  
Blank, if **CustomData** property was not defined at connection time.  
  
## Exceptions  
  
## Remarks  
  
## Example  
The following DAX code verifies if the CustomData property was set to **"OK"**.  
  
```  
=IF(CUSTOMDATA()="OK", "Correct Custom data in connection string", "No custom data in connection string property or unexpected value")  
```  