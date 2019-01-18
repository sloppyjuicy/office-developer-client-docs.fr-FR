---
title: Cancel, méthode (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 791803bb8935ffab24e5aed7e4e6a77360e82b65
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713232"
---
# <a name="cancel-method-ado"></a><span data-ttu-id="5642d-102">Cancel, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="5642d-102">Cancel method (ADO)</span></span>

<span data-ttu-id="5642d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5642d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5642d-104">Annule l'exécution d'un appel de méthode asynchrone en attente.</span><span class="sxs-lookup"><span data-stu-id="5642d-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="5642d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5642d-105">Syntax</span></span>

<span data-ttu-id="5642d-106">*objet*. Annuler</span><span class="sxs-lookup"><span data-stu-id="5642d-106">*object*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="5642d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5642d-107">Remarks</span></span>

<span data-ttu-id="5642d-108">Faites appel à la méthode **Cancel** pour mettre fin à l'exécution d'un appel de méthode asynchrone (à savoir une méthode appelée avec l'option **adAsyncConnect**, **adAsyncExecute** ou **adAsyncFetch** ).</span><span class="sxs-lookup"><span data-stu-id="5642d-108">Use the **Cancel** method to terminate execution of an asynchronous method call (that is, a method invoked with the **adAsyncConnect**, **adAsyncExecute**, or **adAsyncFetch** option).</span></span>

<span data-ttu-id="5642d-109">Le tableau suivant indique quelle tâche est terminée lorsque vous utilisez la méthode **Cancel** sur un type d'objet particulier.</span><span class="sxs-lookup"><span data-stu-id="5642d-109">The following table shows what task is terminated when you use the **Cancel** method on a particular type of object.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<span data-ttu-id="5642d-110">
S'il s'agit d'un <em>objet</em></span><span class="sxs-lookup"><span data-stu-id="5642d-110">If <em>object</em> is a</span></span></p></th>
<th><p><span data-ttu-id="5642d-111">Le dernier appel asynchrone de cette méthode est terminé.</span><span class="sxs-lookup"><span data-stu-id="5642d-111">The last asynchronous call to this method is terminated</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5642d-112"><a href="command-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="5642d-112"><a href="command-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="5642d-113"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></span><span class="sxs-lookup"><span data-stu-id="5642d-113"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5642d-114"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="5642d-114"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="5642d-115"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> ou <a href="open-method-ado-connection.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5642d-115"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> or <a href="open-method-ado-connection.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5642d-116"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="5642d-116"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="5642d-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a> ou <a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5642d-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a>, or <a href="open-method-ado-record.md">Open</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5642d-118"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="5642d-118"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="5642d-119"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5642d-119"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5642d-120"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="5642d-120"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="5642d-121"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5642d-121"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
</tr>
</tbody>
</table>

