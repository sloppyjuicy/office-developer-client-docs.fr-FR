---
title: CursorOptionEnum (référence de base de données du bureau Access)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 211ab4fc9bf4cab6302c8f2bd5f236aecdd0b078
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863648"
---
# <a name="cursoroptionenum"></a><span data-ttu-id="0ccbd-102">CursorOptionEnum</span><span class="sxs-lookup"><span data-stu-id="0ccbd-102">CursorOptionEnum</span></span>

<span data-ttu-id="0ccbd-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ccbd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0ccbd-104">Spécifie la fonctionnalité que la méthode [Supports](supports-method-ado.md) doit tester.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-104">Specifies what functionality the [Supports](supports-method-ado.md) method should test for.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ccbd-105">Constant</span><span class="sxs-lookup"><span data-stu-id="0ccbd-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0ccbd-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ccbd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0ccbd-107">Description</span><span class="sxs-lookup"><span data-stu-id="0ccbd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-108"><strong>adAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-108"><strong>adAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-109">0x1000400</span><span class="sxs-lookup"><span data-stu-id="0ccbd-109">0x1000400</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-110">Prend en charge la méthode <a href="addnew-method-ado.md">AddNew</a> pour l’ajout de nouveaux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-110">Supports the <a href="addnew-method-ado.md">AddNew</a> method to add new records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-111"><strong>adApproxPosition</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-111"><strong>adApproxPosition</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-112">0x4000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-112">0x4000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-113">Prend en charge les propriétés <a href="absoluteposition-property-ado.md">AbsolutePosition</a> et <a href="absolutepage-property-ado.md">AbsolutePage</a>.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-113">Supports the <a href="absoluteposition-property-ado.md">AbsolutePosition</a> and <a href="absolutepage-property-ado.md">AbsolutePage</a> properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-114"><strong>adBookmark</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-114"><strong>adBookmark</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-115">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-116">Prendre en charge la propriété <a href="bookmark-property-ado.md">Bookmark</a> pour l’accès à des enregistrements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-116">Supports the <a href="bookmark-property-ado.md">Bookmark</a> property to gain access to specific records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-117"><strong>adDelete</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-117"><strong>adDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-118">0x1000800</span><span class="sxs-lookup"><span data-stu-id="0ccbd-118">0x1000800</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-119">Prend en charge la méthode <a href="delete-method-ado-recordset.md">Delete</a> pour la suppression d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-119">Supports the <a href="delete-method-ado-recordset.md">Delete</a> method to delete records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-120"><strong>adFind</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-120"><strong>adFind</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-121">0 x 80000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-121">0x80000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-122">Prend en charge la méthode <a href="find-method-ado.md">Find</a> pour localiser une ligne dans un <a href="recordset-object-ado.md">Recordset</a>.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-122">Supports the <a href="find-method-ado.md">Find</a> method to locate a row in a <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-123"><strong>adHoldRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-123"><strong>adHoldRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-124">0 x 100</span><span class="sxs-lookup"><span data-stu-id="0ccbd-124">0x100</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-125">Recherche d'autres enregistrements ou modifie la position suivante sans valider les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-125">Retrieves more records or changes the next position without committing all pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-126"><strong>adIndex</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-126"><strong>adIndex</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-127">0 x 100000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-127">0x100000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-128">Prend en charge la propriété <a href="index-property-ado.md">Index</a> pour nommer un index.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-128">Supports the <a href="index-property-ado.md">Index</a> property to name an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-129"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-129"><strong>adMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-130">0 x 200</span><span class="sxs-lookup"><span data-stu-id="0ccbd-130">0x200</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-131">Prend en charge les méthodes <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> et <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a>, ainsi que les méthodes <a href="move-method-ado.md">Move</a> ou <a href="getrows-method-ado.md">GetRows</a> pour faire reculer la position de l’enregistrement en cours sans nécessiter de signets.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-131">Supports the <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> and <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> methods, and <a href="move-method-ado.md">Move</a> or <a href="getrows-method-ado.md">GetRows</a> methods to move the current record position backward without requiring bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-132"><strong>adNotify</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-132"><strong>adNotify</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-133">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-133">0x40000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-134">Indique que le fournissseur de données sous-jacentes prend en charge les notifications (ce qui détermine la prise en charge des événements <strong>Recordset</strong>).</span><span class="sxs-lookup"><span data-stu-id="0ccbd-134">Indicates that the underlying data provider supports notifications (which determines whether <strong>Recordset</strong> events are supported).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-135"><strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-135"><strong>adResync</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-136">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-136">0x20000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-137">Prend en charge la méthode <a href="resync-method-ado.md">Resync</a> pour mettre à jour le curseur avec les données visibles dans la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-137">Supports the <a href="resync-method-ado.md">Resync</a> method to update the cursor with the data that is visible in the underlying database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-138"><strong>adSeek</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-138"><strong>adSeek</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-139">0x200000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-139">0x200000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-140">Prend en charge la méthode <a href="seek-method-ado.md">Seek</a> pour localiser une ligne dans <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-140">Supports the <a href="seek-method-ado.md">Seek</a> method to locate a row in a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-141"><strong>adUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-141"><strong>adUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-142">0x1008000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-142">0x1008000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-143">Prend en charge la méthode <a href="update-method-ado.md">Update</a> pour modifier des données existantes.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-143">Supports the <a href="update-method-ado.md">Update</a> method to modify existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-144"><strong>adUpdateBatch</strong></span><span class="sxs-lookup"><span data-stu-id="0ccbd-144"><strong>adUpdateBatch</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccbd-145">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="0ccbd-145">0x10000</span></span></p></td>
<td><p><span data-ttu-id="0ccbd-146">Prend en charge la mise à jour par lots (méthodes <a href="updatebatch-method-ado.md">UpdateBatch</a> et <a href="cancelbatch-method-ado.md">CancelBatch</a>) pour transmettre des groupes de modifications au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-146">Supports batch updating (<a href="updatebatch-method-ado.md">UpdateBatch</a> and <a href="cancelbatch-method-ado.md">CancelBatch</a> methods) to transmit groups of changes to the provider.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0ccbd-147">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0ccbd-147">ADO/WFC equivalent</span></span>

<span data-ttu-id="0ccbd-148">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0ccbd-148">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ccbd-149">Constante</span><span class="sxs-lookup"><span data-stu-id="0ccbd-149">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-150">AdoEnums.CursorOption.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="0ccbd-150">AdoEnums.CursorOption.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-151">AdoEnums.CursorOption.APPROXPOSITION</span><span class="sxs-lookup"><span data-stu-id="0ccbd-151">AdoEnums.CursorOption.APPROXPOSITION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-152">AdoEnums.CursorOption.BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="0ccbd-152">AdoEnums.CursorOption.BOOKMARK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-153">AdoEnums.CursorOption.DELETE</span><span class="sxs-lookup"><span data-stu-id="0ccbd-153">AdoEnums.CursorOption.DELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-154">AdoEnums.CursorOption.FIND</span><span class="sxs-lookup"><span data-stu-id="0ccbd-154">AdoEnums.CursorOption.FIND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-155">AdoEnums.CursorOption.HOLDRECORDS</span><span class="sxs-lookup"><span data-stu-id="0ccbd-155">AdoEnums.CursorOption.HOLDRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-156">AdoEnums.CursorOption.INDEX</span><span class="sxs-lookup"><span data-stu-id="0ccbd-156">AdoEnums.CursorOption.INDEX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-157">AdoEnums.CursorOption.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="0ccbd-157">AdoEnums.CursorOption.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-158">AdoEnums.CursorOption.NOTIFY</span><span class="sxs-lookup"><span data-stu-id="0ccbd-158">AdoEnums.CursorOption.NOTIFY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-159">AdoEnums.CursorOption.RESYNC</span><span class="sxs-lookup"><span data-stu-id="0ccbd-159">AdoEnums.CursorOption.RESYNC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-160">AdoEnums.CursorOption.SEEK</span><span class="sxs-lookup"><span data-stu-id="0ccbd-160">AdoEnums.CursorOption.SEEK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccbd-161">AdoEnums.CursorOption.UPDATE</span><span class="sxs-lookup"><span data-stu-id="0ccbd-161">AdoEnums.CursorOption.UPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ccbd-162">AdoEnums.CursorOption.UPDATEBATCH</span><span class="sxs-lookup"><span data-stu-id="0ccbd-162">AdoEnums.CursorOption.UPDATEBATCH</span></span></p></td>
</tr>
</tbody>
</table>

