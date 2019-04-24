---
title: Recordset2. BatchSize, propriété (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f615823f99e2fdaa50a051d89a90c8f85a6ec841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307468"
---
# <a name="recordset2batchsize-property-dao"></a><span data-ttu-id="f4b18-102">Recordset2. BatchSize, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="f4b18-102">Recordset2.BatchSize property (DAO)</span></span>


<span data-ttu-id="f4b18-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4b18-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f4b18-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4b18-104">Syntax</span></span>

<span data-ttu-id="f4b18-105">*expression* . BatchSize</span><span class="sxs-lookup"><span data-stu-id="f4b18-105">*expression* .BatchSize</span></span>

<span data-ttu-id="f4b18-106">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="f4b18-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4b18-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4b18-107">Remarks</span></span>

<span data-ttu-id="f4b18-p101">La propriété **BatchSize** détermine la taille de lot utilisée lors de l'envoi d'instructions au serveur dans une mise à jour par lot. La valeur de la propriété détermine le nombre d'instructions envoyées au serveur dans un seul tampon de commandes. Par défaut, 15 instructions sont envoyées au serveur dans chaque lot. Cette propriété peut être modifiée à tout moment. Si un serveur de base de données ne prend pas en charge l'envoi d'instructions par lot, vous pouvez affecter à cette propriété la valeur 1, chaque instruction étant, dans ce cas, envoyée séparément.</span><span class="sxs-lookup"><span data-stu-id="f4b18-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="f4b18-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="f4b18-113">Example</span></span>

<span data-ttu-id="f4b18-114">Cet exemple utilise les propriétés **BatchSize** et **UpdateOptions** pour contrôler certains aspects de la la mise à jour par lot de l'objet Recordset spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4b18-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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

