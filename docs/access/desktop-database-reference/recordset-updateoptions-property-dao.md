---
title: Recordset.UpdateOptions Property (DAO)
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
ms.openlocfilehash: 065ca41d46f50911835d79989e39636b62b30b97
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471050"
---
# <a name="recordsetupdateoptions-property-dao"></a><span data-ttu-id="98128-102">Recordset.UpdateOptions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="98128-102">Recordset.UpdateOptions Property (DAO)</span></span>


<span data-ttu-id="98128-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98128-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="98128-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98128-104">Syntax</span></span>

<span data-ttu-id="98128-105">*expression* . UpdateOptions (OptionsMAJ)</span><span class="sxs-lookup"><span data-stu-id="98128-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="98128-106">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="98128-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="98128-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="98128-107">Remarks</span></span>

<span data-ttu-id="98128-108">Lorsqu'une méthode **[Update](recordset-update-method-dao.md)** en mode de traitement par lot est exécutée, DAO et la bibliothèque client de curseurs par lots créent une série d'instructions SQL UPDATE pour apporter les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="98128-108">When a batch-mode **[Update](recordset-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="98128-109">Une clause SQL WHERE est créée pour chaque mise à jour afin d'isoler les enregistrements marqués comme étant modifiés par la propriété **[RecordStatus](recordset-recordstatus-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="98128-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="98128-110">Dans la mesure où certains serveurs distants utilisent des déclencheurs ou d'autres moyens pour appliquer l'intégrité référentielle, il est souvent essentiel de limiter les champs à mettre à jour aux seuls champs affectés par la modification.</span><span class="sxs-lookup"><span data-stu-id="98128-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="98128-111">Pour ce faire, affectez à la propriété **UpdateOptions** l'une des constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="98128-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="98128-112">De cette façon, seule la partie minimale indispensable du code de déclencheur est exécutée.</span><span class="sxs-lookup"><span data-stu-id="98128-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="98128-113">Ainsi, l'opération de mise à jour est exécutée plus rapidement et est moins susceptible de contenir des erreurs.</span><span class="sxs-lookup"><span data-stu-id="98128-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="98128-p103">h **dbCriteriaDeleteInsert** **dbCriteriaUpdate** **UpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="98128-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="98128-117">Si vous ne spécifiez pas de constantes, **dbCriteriaUpdate** et **dbCriteriaKey** seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="98128-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="98128-118">Les enregistrements récemment ajoutés génèreront toujours des instructions INSERT et les enregistrements supprimés génèreront toujours des instructions DELETE ; cette propriété ne s'applique donc qu'à la manière dont les mises à jour des bibliothèques de curseurs mettent à jour les enregistrements modifiés.</span><span class="sxs-lookup"><span data-stu-id="98128-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

## <a name="example"></a><span data-ttu-id="98128-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="98128-119">Example</span></span>

<span data-ttu-id="98128-120">Cet exemple utilise les propriétés **BatchSize** et **UpdateOptions** pour contrôler des aspects des mises à jour par lot pour l'objet **Recordset** spécifié.</span><span class="sxs-lookup"><span data-stu-id="98128-120">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified **Recordset** object.</span></span>

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

