---
title: Recordset2.BatchSize Property (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c0d97b6727f8f294bb2a778423ca02666b7d05f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472579"
---
# <a name="recordset2batchsize-property-dao"></a><span data-ttu-id="9ac3a-102">Recordset2.BatchSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ac3a-102">Recordset2.BatchSize Property (DAO)</span></span>


<span data-ttu-id="9ac3a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ac3a-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac3a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ac3a-104">Syntax</span></span>

<span data-ttu-id="9ac3a-105">*expression* . BatchSize</span><span class="sxs-lookup"><span data-stu-id="9ac3a-105">*expression* .BatchSize</span></span>

<span data-ttu-id="9ac3a-106">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="9ac3a-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac3a-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ac3a-107">Remarks</span></span>

<span data-ttu-id="9ac3a-p101">La propriété **BatchSize** détermine la taille de lot utilisée lors de l'envoi des instructions au serveur dans une mise à jour par lot. La valeur de la propriété détermine le nombre d'instructions envoyées au serveur dans un tampon de commande. Par défaut, 15 instructions sont envoyées au serveur dans chaque lot. Il est possible de modifier cette propriété à tout moment. Si un serveur de base de données ne prend pas en charge les lots d'instructions, vous pouvez définir cette propriété sur la valeur 1. Chaque instruction est alors envoyée séparément.</span><span class="sxs-lookup"><span data-stu-id="9ac3a-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="9ac3a-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="9ac3a-113">Example</span></span>

<span data-ttu-id="9ac3a-114">L'exemple ci-dessous utilise les propriétés **BatchSize** et **UpdateOptions** pour déterminer les aspects des mises à jour par lot pour l'objet Recordset spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ac3a-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

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

