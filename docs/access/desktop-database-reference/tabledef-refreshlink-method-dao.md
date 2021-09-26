---
title: TableDef.RefreshLink method (DAO)
TOCTitle: RefreshLink Method
ms:assetid: 9f0059c6-3b7b-57e3-7527-ef674ad9417d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198349(v=office.15)
ms:contentKeyID: 48546674
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052980
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3092a623dc84726c4f2d217c0eaea40546b48627
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631692"
---
# <a name="tabledefrefreshlink-method-dao"></a>TableDef.RefreshLink method (DAO)

**S’applique à** : Access 2013, Office 2013
 
Met à jour les informations de connexion d’une table liée (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* RefreshLink

*expression* Variable représentant un objet **TableDef**.

## <a name="remarks"></a>Remarques

Pour modifier les informations de connexion pour une table liée, réinitialisez la propriété **[Connect](connection-connect-property-dao.md)** de l'objet **TableDef** correspondant, puis utilisez la méthode **RefreshLink** pour mettre à jour les informations. L'utilisation de la méthode **RefreshLink** ne modifie pas les propriétés de la table liée et les objets **[Relation](relation-object-dao.md)**.

Pour que ces informations de connexion existent dans toutes les connexions associées à l'objet **TableDef** qui représente la table liée, vous devez utiliser la méthode **[Refresh](tabledefs-refresh-method-dao.md)** dans chaque collection.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **RefreshLink** pour actualiser les données dans une table liée une fois que sa connexion a été modifiée d'une source de données vers une autre. La procédure RefreshLinkOutput est nécessaire à l'exécution de cette procédure.

```vb 
Sub RefreshLinkX() 
 
 Dim dbsCurrent As Database 
 Dim tdfLinked As TableDef 
 
 ' Open a database to which a linked table can be 
 ' appended. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a linked table that points to a Microsoft 
 ' SQL Server database. 
 Set tdfLinked = _ 
 dbsCurrent.CreateTableDef("AuthorsTable") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 tdfLinked.SourceTableName = "authors" 
 dbsCurrent.TableDefs.Append tdfLinked 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to first source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Change connection information for linked table and 
 ' refresh the connection in order to make the new data 
 ' available. 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=NewPublishers" 
 tdfLinked.RefreshLink 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to second source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Delete linked table because this is a demonstration. 
 dbsCurrent.TableDefs.Delete tdfLinked.Name 
 
 dbsCurrent.Close 
 
End Sub 
 
Sub RefreshLinkOutput(dbsTemp As Database) 
 
 Dim rstRemote As Recordset 
 Dim intCount As Integer 
 
 ' Open linked table. 
 Set rstRemote = _ 
 dbsTemp.OpenRecordset("AuthorsTable") 
 
 intCount = 0 
 
 ' Enumerate Recordset object, but stop at 50 records. 
 With rstRemote 
 Do While Not .EOF And intCount < 50 
 Debug.Print , .Fields(0), .Fields(1) 
 intCount = intCount + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[more records]" 
 .Close 
 End With 
 
End Sub 
 
```

