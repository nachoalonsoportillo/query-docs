---
title: "List.Split | Microsoft Docs"
ms.date: 5/22/2018
ms.prod: power-query
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# List.Split

<code>List.Split(<b>list</b> as list, <b>pageSize</b> as number) as list</code>

## About
Splits <code>list</code> into a list of lists where the first element of the output list is a list containing the first <code>pageSize</code> elements from the source list, the next element of the output list is a list containing the next <code>pageSize</code> elements from the source list, etc.