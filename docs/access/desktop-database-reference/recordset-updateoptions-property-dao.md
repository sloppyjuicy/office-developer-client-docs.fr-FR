---
title: Propriété Recordset.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ced8fc78729924ce271aa0fe38d77d287a131f13
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705938"
---
# <a name="recordsetupdateoptions-property-dao"></a>Propriété Recordset.UpdateOptions (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . UpdateOptions (OptionsMAJ)

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Lorsqu'une méthode **[Update](recordset-update-method-dao.md)** en mode de traitement par lot est exécutée, DAO et la bibliothèque client de curseurs par lots créent une série d'instructions SQL UPDATE pour apporter les modifications nécessaires. Une clause SQL WHERE est créée pour chaque mise à jour afin d'isoler les enregistrements marqués comme étant modifiés par la propriété **[RecordStatus](recordset-recordstatus-property-dao.md)**. Dans la mesure où certains serveurs distants utilisent des déclencheurs ou d'autres moyens pour appliquer l'intégrité référentielle, il est souvent essentiel de limiter les champs à mettre à jour aux seuls champs affectés par la modification. 

Pour ce faire, affectez à la propriété **UpdateOptions** l'une des constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**. De cette façon, seule la partie minimale indispensable du code de déclencheur est exécutée. Ainsi, l'opération de mise à jour est exécutée plus rapidement et est moins susceptible de contenir des erreurs.

h **dbCriteriaDeleteInsert** **dbCriteriaUpdate** **UpdateOptions**

Si vous ne spécifiez pas de constantes, **dbCriteriaUpdate** et **dbCriteriaKey** seront utilisées.

Les enregistrements récemment ajoutés génèreront toujours des instructions INSERT et les enregistrements supprimés génèreront toujours des instructions DELETE ; cette propriété ne s'applique donc qu'à la manière dont les mises à jour des bibliothèques de curseurs mettent à jour les enregistrements modifiés.

## <a name="example"></a>Exemple

Cet exemple utilise les propriétés **BatchSize** et **UpdateOptions** pour contrôler des aspects des mises à jour par lot pour l'objet **Recordset** spécifié.

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

