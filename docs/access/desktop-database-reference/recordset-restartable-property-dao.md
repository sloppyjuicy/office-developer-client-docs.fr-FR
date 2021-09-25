---
title: Recordset.Restartable, propriété (DAO)
TOCTitle: Restartable Property
ms:assetid: 00def49d-ea7e-6cd5-2f4a-914a1ddcdd51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844737(v=office.15)
ms:contentKeyID: 48542919
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052926
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: e0af1932a625703c08f7b0c873c177e21bd14ed0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572878"
---
# <a name="recordsetrestartable-property-dao"></a>Recordset.Restartable, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur indiquant si un objet **[Recordset](recordset-object-dao.md)** prend en charge la méthode **[Requery](recordset-requery-method-dao.md)**, laquelle réexécute la requête sur laquelle l'objet **Recordset** est basé.

## <a name="syntax"></a>Syntaxe

*.* Restartable

*expression* Variable qui représente un objet **Recordset**.

## <a name="remarks"></a>Remarques

Les objets **Recordset** de type table renvoient toujours la valeur **False**.

Vérifiez la propriété **Restartable** avant d'utiliser la méthode **Requery** sur un objet **Recordset**. Si la propriété **Restartable** a la valeur **False**, appelez la méthode **[OpenRecordset](connection-openrecordset-method-dao.md)** sur l'objet **[QueryDef](querydef-object-dao.md)** sous-jacent pour réexécuter la requête.

## <a name="example"></a>Exemple

Cet exemple illustre l'utilisation de la propriété **Restartable** avec différents objets **Recordset**.

```vb
    Sub RestartableX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTemp As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open a table-type Recordset and print its 
     ' Restartable property. 
     Set rstTemp = .OpenRecordset("Employees", dbOpenTable) 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from an SQL statement and print its 
     ' Restartable property. 
     Set rstTemp = _ 
     .OpenRecordset("SELECT * FROM Employees") 
     Debug.Print "Recordset based on SQL statement" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from a saved QueryDef object and 
     ' print its Restartable property. 
     Set rstTemp = .OpenRecordset("Current Product List") 
     Debug.Print _ 
     "Recordset based on permanent QueryDef (" & _ 
     rstTemp.Name & ")" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     .Close 
     End With 
     
    End Sub
```
