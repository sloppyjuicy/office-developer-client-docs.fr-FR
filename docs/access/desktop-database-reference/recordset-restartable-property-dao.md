---
title: Propriété Recordset.Restartable (DAO)
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
ms.openlocfilehash: 26d9d215c35e9a768a663d41ecc40f49bee4dfdb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920857"
---
# <a name="recordsetrestartable-property-dao"></a>Propriété Recordset.Restartable (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie une valeur indiquant si un objet **[Recordset](recordset-object-dao.md)** prend en charge la méthode **[Requery](recordset-requery-method-dao.md)**, laquelle réexécute la requête sur laquelle l'objet **Recordset** est basé.

## <a name="syntax"></a>Syntaxe

*expression* . Restartable

*expression* Variable qui représente un objet **Recordset** .

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
