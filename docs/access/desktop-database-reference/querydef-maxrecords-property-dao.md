---
title: Propriété QueryDef.MaxRecords (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: bc89dd8460117b117699957e09c7b9aa4cce0223
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622010"
---
# <a name="querydefmaxrecords-property-dao"></a>Propriété QueryDef.MaxRecords (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie le nombre maximum d'enregistrements à renvoyer pour une requête sur une source de données ODBC.

## <a name="syntax"></a>Syntaxe

*.* MaxRecords

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

La valeur par défaut est 0, indiquant que le nombre d'enregistrements renvoyés est illimité.

Une fois que le nombre de lignes spécifié par **MaxRecords** est renvoyé à votre application dans un objet **[Recordset](recordset-object-dao.md)**, le gestionnaire de requêtes arrête son traitement même si d'autres enregistrements pourraient être inclus dans l'objet **Recordset**. Cette propriété est utile dans les cas où les ressources client limitées empêchent la gestion de grandes quantités d'enregistrements.

> [!NOTE]
> [!REMARQUE] La propriété **MaxRecords** est compatible uniquement avec une source de données ODBC.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **MaxRecords** pour limiter le nombre maximal des enregistrements renvoyés par une requête sur une source de données ODBC.

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

