---
title: "PATHITEM Function (DAX) | Microsoft Docs"
ms.prod: dax
ms.date: 5/22/2018
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# PATHITEM Function (DAX)
Returns the item at the specified *position* from a string resulting from evaluation of a PATH function. Positions are counted from left to right.  
  
## Syntax  
  
```  
PATHITEM(<path>, <position>[, <type>])  
```  
  
#### Parameters  
path  
A text string in the form of the results of a PATH function.  
  
position  
An integer expression with the position of the item to be returned.  
  
type  
(Optional)An enumeration that defines the data type of the result:  
  
||||  
|-|-|-|  
|**Enumeration**|**Alternate Enumeration**|**Description**|  
|TEXT|0|Results are returned with the data type text. (default).|  
|INTEGER|1|Results are returned as integers.|  
  
## Return Value  
The identifier returned by the PATH function at the specified position in the list of identifiers. Items returned by the PATH function are ordered by most distant to current.  
  
## Remarks  
  
-   This function can be used to return a specific level from a hierarchy returned by a PATH function. For example, you could return just the skip-level managers for all employees.  
  
-   If you specify a number for *position* that is less than one (1) or greater than the number of elements in *path*, the PATHITEM function returns BLANK  
  
-   If *type* is not a valid enumeration element an error is returned.  
  
This DAX function is not supported for use in DirectQuery mode. For more information about limitations in DirectQuery models, see  [http://go.microsoft.com/fwlink/?LinkId=219172](http://go.microsoft.com/fwlink/?LinkId=219172).  
  
## Example  
The following example returns the third tier manager of the current employee; it takes the employee and manager IDs as the input to a PATH function that returns a string with the hierarchy of parents to current employee. From that string PATHITEM returns the third entry as an integer.  
  
```  
=PATHITEM(PATH(Employee[EmployeeKey], Employee[ParentEmployeeKey]), 3, 1)  
```  