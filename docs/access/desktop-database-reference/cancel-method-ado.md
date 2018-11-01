---
title: Cancel, méthode (ADO)
TOCTitle: Cancel Method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8ebdfe912f8a440f8935834256d4279a39f840f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888383"
---
# <a name="cancel-method-ado"></a><span data-ttu-id="44840-102">Cancel, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="44840-102">Cancel Method (ADO)</span></span>


<span data-ttu-id="44840-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44840-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44840-104">Annule l'exécution d'un appel de méthode asynchrone en attente.</span><span class="sxs-lookup"><span data-stu-id="44840-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="44840-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44840-105">Syntax</span></span>

<span data-ttu-id="44840-106">*objet*. Annuler</span><span class="sxs-lookup"><span data-stu-id="44840-106">*object*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="44840-107">Notes</span><span class="sxs-lookup"><span data-stu-id="44840-107">Remarks</span></span>

<span data-ttu-id="44840-108">Faites appel à la méthode **Cancel** pour mettre fin à l'exécution d'un appel de méthode asynchrone (à savoir une méthode appelée avec l'option **adAsyncConnect**, **adAsyncExecute** ou **adAsyncFetch** ).</span><span class="sxs-lookup"><span data-stu-id="44840-108">Use the **Cancel** method to terminate execution of an asynchronous method call (that is, a method invoked with the **adAsyncConnect**, **adAsyncExecute**, or **adAsyncFetch** option).</span></span>

<span data-ttu-id="44840-109">Le tableau suivant indique quelle tâche est terminée lorsque vous utilisez la méthode **Cancel** sur un type d'objet particulier.</span><span class="sxs-lookup"><span data-stu-id="44840-109">The following table shows what task is terminated when you use the **Cancel** method on a particular type of object.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<span data-ttu-id="44840-110">
S'il s'agit d'un <em>objet</em></span><span class="sxs-lookup"><span data-stu-id="44840-110">If <em>object</em> is a</span></span></p></th>
<th><p><span data-ttu-id="44840-111">Le dernier appel asynchrone de cette méthode est terminé.</span><span class="sxs-lookup"><span data-stu-id="44840-111">The last asynchronous call to this method is terminated</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44840-112"><a href="command-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="44840-112"><a href="command-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="44840-113"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</a></span><span class="sxs-lookup"><span data-stu-id="44840-113"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44840-114"><a href="connection-object-ado.md">Objet Connection</a></span><span class="sxs-lookup"><span data-stu-id="44840-114"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="44840-115"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</a> ou <a href="open-method-ado-connection.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="44840-115"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</a> or <a href="open-method-ado-connection.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44840-116"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="44840-116"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="44840-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a> ou <a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="44840-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a>, or <a href="open-method-ado-record.md">Open</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44840-118"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="44840-118"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="44840-119"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="44840-119"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44840-120"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="44840-120"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="44840-121"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="44840-121"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
</tr>
</tbody>
</table>

