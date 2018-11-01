---
title: Recordset.BatchCollisionCount Property (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 9d166463-8313-c0f5-8389-5d5ad933eb33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198240(v=office.15)
ms:contentKeyID: 48546617
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101181
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 079da0d4e489b4082283c78bc9e84b7d95959e82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883308"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a><span data-ttu-id="9159a-102">Recordset.BatchCollisionCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9159a-102">Recordset.BatchCollisionCount Property (DAO)</span></span>


<span data-ttu-id="9159a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9159a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9159a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9159a-104">Syntax</span></span>

<span data-ttu-id="9159a-105">*expression* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="9159a-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="9159a-106">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="9159a-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9159a-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="9159a-107">Remarks</span></span>

<span data-ttu-id="9159a-p101">Cette propriété indique le nombre d'enregistrements qui ont subi des collisions ou qui n'ont pas été mis à jour lors de la dernière mise à jour par lot. La valeur de cette propriété correspond au nombre de signets de la propriété **[BatchCollisions](recordset-batchcollisions-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9159a-p101">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt. The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="9159a-110">Si vous définissez la propriété **[Bookmark](recordset-object-dao.md)** de l'objet **[Recordset](recordset-bookmark-property-dao.md)** de travail sur des signets du tableau **BatchCollisions**, vous pouvez accéder à chaque enregistrement dont la dernière opération **[Update](recordset-update-method-dao.md)** par lot a échoué.</span><span class="sxs-lookup"><span data-stu-id="9159a-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="9159a-p102">Une fois les enregistrements en collision corrigés, il est possible de rappeler une méthode **Update** en mode par lot. À ce stade, DAO tente d'exécuter une autre mise à jour par lot et la propriété **BatchCollisions** indique à nouveau le jeu d'enregistrements dont la seconde tentative a échoué. Les enregistrements dont la tentative précédente a réussi ne sont pas envoyés dans la tentative en cours, car ils possèdent à présent la propriété **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified. Ce processus peut se poursuivre jusqu'à ce que toutes les collisions soient résolues ou que vous abandonniez les mises à jour et fermiez le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="9159a-p102">After the collision records are corrected, a batch-mode **Update** method can be called again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="9159a-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="9159a-115">Example</span></span>

<span data-ttu-id="9159a-116">L'exemple ci-dessous fait appel à la propriété **BatchCollisionCount** et à la méthode **Update** pour illustrer la mise à jour par lot où toutes les collisions sont résolues en forçant la mise à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="9159a-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
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

