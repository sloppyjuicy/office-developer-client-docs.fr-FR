---
title: Propriété Recordset2.BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 997dfbb3-673c-8813-f51b-ab8d95093c4f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197961(v=office.15)
ms:contentKeyID: 48546514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33650b9fdbaf7fbc9266c8c778199e1138cd5b21
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706652"
---
# <a name="recordset2batchcollisioncount-property-dao"></a>Propriété Recordset2.BatchCollisionCount (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . BatchCollisionCount

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Cette propriété indique le nombre d'enregistrements dont la mise à jour a échoué en raison de conflits ou pour un autre motif lors de la dernière tentative de mise à jour par lot. La valeur de cette propriété correspond au nombre de signets dans la propriété **[BatchCollisions](recordset2-batchcollisions-property-dao.md)**.

Si vous affectez à la propriété [**Bookmark**](recordset2-bookmark-property-dao.md) de l'objet **Recordset** de travail des valeurs de signet du tableau **BatchCollisions**, vous pouvez accéder à chaque enregistrement qui n'a pas pu achever la dernière opération **[Update](recordset2-update-method-dao.md)** par lot.

Après correction des enregistrements présentant des conflits, il est possible d'appeler à nouveau une méthode **Update** en mode batch. À ce stade, DAO tente d'exécuter une autre mise à jour par lot et la propriété **BatchCollisions** reflète à nouveau le jeu d'enregistrements ayant échoué à la deuxième tentative. Tous les enregistrements dont la mise à jour a réussi lors de la tentative précédente ne sont pas repris dans la tentative actuelle car leur propriété **[RecordStatus](recordset2-recordstatus-property-dao.md)** a désormais la valeur **dbRecordUnmodified**. Ce processus peut se poursuivre aussi longtemps que des conflits surviennent ou jusqu'à ce que vous abandonniez les mises à jour et fermiez le jeu de résultats.

## <a name="example"></a>Exemple

L'exemple ci-dessous fait appel à la propriété **BatchCollisionCount** et à la méthode **Update** pour illustrer la mise à jour par lot où toutes les collisions sont résolues en forçant la mise à jour par lot.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
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
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

