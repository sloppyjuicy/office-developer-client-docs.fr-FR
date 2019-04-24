---
title: Recordsets, collection (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b935e05264497c7ad09ada4a8c50c775845857b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309302"
---
# <a name="recordsets-collection-dao"></a>Recordsets, collection (DAO)

**S’applique à** : Access 2013, Office 2013

Une collection **Recordsets** contient tous les objets **Recordset** ouverts, dans un objet **Connection** ou **Database**.

## <a name="remarks"></a>Remarques

Lorsque vous utilisez des objets DAO, vous manipulez les données presque exclusivement à l'aide des objets **Recordset**.

Un objet **Recordset** est automatiquement ajouté à la collection **Recordsets** lorsque vous ouvrez l'objet **Recordset** et supprimé lorsque vous le fermez.

Vous pouvez créer autant de variables d'objet **Recordset** que vous le souhaitez. Des objets **Recordset** différents peuvent accéder aux mêmes tables, requêtes et champs sans créer de conflits.

Pour faire référence à un objet **Recordset** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :

- **Recordsets**(0)

- **Jeux d'enregistrements** ("nom")

- **Nom des jeux d'enregistrements**\!\[\]

> [!NOTE]
> [!REMARQUE] Vous pouvez ouvrir plusieurs fois un objet **Recordset** à partir de la même source de données ou base de données en créant des noms en double dans la collection **Recordsets**. Vous devez attribuer des objets **Recordset** à des variables d'objet et y faire référence par nom de variable.

## <a name="example"></a>Exemple

L'exemple ci-dessous illustre les objets **Recordset** et la collection **Recordsets** en ouvrant quatre types d'objet **Recordsets** différents, en énumérant la collection Recordsets de l'objet **Database** actif et en énumérant la collection **Properties** de chaque objet **Recordset**.

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
