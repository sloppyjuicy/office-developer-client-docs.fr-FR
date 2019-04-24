---
title: CursorTypeEnum (référence de base de données de bureau Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295162"
---
# <a name="cursortypeenum"></a><span data-ttu-id="0f466-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="0f466-102">CursorTypeEnum</span></span>

<span data-ttu-id="0f466-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f466-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f466-104">Spécifie le type de curseur utilisé dans un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0f466-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f466-105">Constante</span><span class="sxs-lookup"><span data-stu-id="0f466-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0f466-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f466-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0f466-107">Description</span><span class="sxs-lookup"><span data-stu-id="0f466-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f466-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="0f466-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="0f466-109">n°2</span><span class="sxs-lookup"><span data-stu-id="0f466-109">2</span></span></p></td>
<td><p><span data-ttu-id="0f466-p101">Utilise un curseur dynamique. Les ajouts, les modifications et les suppressions effectués par d’autres utilisateurs sont visibles, et tous les types de déplacement dans l’objet <strong>Recordset</strong> sont permis, à l’exception des signets, si le fournisseur ne les prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="0f466-p101">Uses a dynamic cursor. Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f466-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="0f466-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="0f466-113">0</span><span class="sxs-lookup"><span data-stu-id="0f466-113">0</span></span></p></td>
<td><p><span data-ttu-id="0f466-p102">Par défaut. Utilise un curseur "descendant". Identique au curseur statique, sauf que vous ne pouvez que descendre dans les enregistrements. Les performances sont améliorées si vous n'avez besoin de ne passer qu'une fois dans l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f466-p102">Default. Uses a forward-only cursor. Identical to a static cursor, except that you can only scroll forward through records. This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f466-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="0f466-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="0f466-119">0,1</span><span class="sxs-lookup"><span data-stu-id="0f466-119">1</span></span></p></td>
<td><p><span data-ttu-id="0f466-p103">Utilise un curseur keyset. Identique à un curseur dynamique, sauf que vous ne pouvez pas voir les enregistrements ajoutés par d'autres utilisateurs, bien que les enregistrements supprimés par d'autres utilisateurs ne soient pas accessibles par votre <strong>Recordset</strong>. Les modifications apportées aux données par d'autres utilisateurs sont toujours visibles.</span><span class="sxs-lookup"><span data-stu-id="0f466-p103">Uses a keyset cursor. Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>. Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f466-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="0f466-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="0f466-124">3</span><span class="sxs-lookup"><span data-stu-id="0f466-124">3</span></span></p></td>
<td><p><span data-ttu-id="0f466-p104">Utilise un curseur statique. Il s'agit d"une copie statique d'un ensemble d'enregistrements, que vous pouvez utiliser pour trouver des données ou générer des rapports. Les ajouts, les modifications et les suppressions effectués par d'autres utiisateurs ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="0f466-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f466-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="0f466-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="0f466-129">-1</span><span class="sxs-lookup"><span data-stu-id="0f466-129">-1</span></span></p></td>
<td><p><span data-ttu-id="0f466-130">Ne spécifie pas le type du curseur.</span><span class="sxs-lookup"><span data-stu-id="0f466-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0f466-131">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0f466-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="0f466-132">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0f466-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f466-133">Constante</span><span class="sxs-lookup"><span data-stu-id="0f466-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f466-134">AdoEnums. CursorType. DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="0f466-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f466-135">AdoEnums. CursorType. FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="0f466-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f466-136">AdoEnums. CursorType. KEYSet</span><span class="sxs-lookup"><span data-stu-id="0f466-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f466-137">AdoEnums. CursorType. STATIC</span><span class="sxs-lookup"><span data-stu-id="0f466-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f466-138">AdoEnums. CursorType. unSPÉCIFIÉ</span><span class="sxs-lookup"><span data-stu-id="0f466-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

