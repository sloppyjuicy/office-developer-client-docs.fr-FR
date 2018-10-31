---
title: IsolationLevelEnum (référence de base de données du bureau Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7e32cd3c8ae78199f90fcac8cccdf377bf332d38
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863940"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="1a594-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="1a594-102">IsolationLevelEnum</span></span>

<span data-ttu-id="1a594-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a594-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1a594-104">Spécifie le niveau d'isolement de transaction d'un objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1a594-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a594-105">Constant</span><span class="sxs-lookup"><span data-stu-id="1a594-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1a594-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a594-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1a594-107">Description</span><span class="sxs-lookup"><span data-stu-id="1a594-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a594-108"><strong>: adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-109">-1</span><span class="sxs-lookup"><span data-stu-id="1a594-109">-1</span></span></p></td>
<td><p><span data-ttu-id="1a594-110">Indique que le fournisseur applique un niveau d’isolement différent de celui spécifié, mais que ce niveau ne peut être déterminé.</span><span class="sxs-lookup"><span data-stu-id="1a594-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a594-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-112">16</span><span class="sxs-lookup"><span data-stu-id="1a594-112">16</span></span></p></td>
<td><p><span data-ttu-id="1a594-113">Indique que les modifications en attente de transactions mieux isolées ne peuvent être remplacées.</span><span class="sxs-lookup"><span data-stu-id="1a594-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a594-114"><strong>à adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-115">256</span><span class="sxs-lookup"><span data-stu-id="1a594-115">256</span></span></p></td>
<td><p><span data-ttu-id="1a594-116">Indique qu'à partir d'une transaction, vous pouvez visualiser les modifications non validées des autres transactions.</span><span class="sxs-lookup"><span data-stu-id="1a594-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a594-117"><strong>valeur adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-118">256</span><span class="sxs-lookup"><span data-stu-id="1a594-118">256</span></span></p></td>
<td><p><span data-ttu-id="1a594-119">Identique à <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a594-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a594-120"><strong>à adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-121">4096</span><span class="sxs-lookup"><span data-stu-id="1a594-121">4096</span></span></p></td>
<td><p><span data-ttu-id="1a594-122">Indique qu'à partir d'une transaction, vous pouvez visualiser les modifications d'autres transactions uniquement si elles ont été validées.</span><span class="sxs-lookup"><span data-stu-id="1a594-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a594-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-124">4096</span><span class="sxs-lookup"><span data-stu-id="1a594-124">4096</span></span></p></td>
<td><p><span data-ttu-id="1a594-125">Identique à <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a594-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a594-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-127">65536</span><span class="sxs-lookup"><span data-stu-id="1a594-127">65536</span></span></p></td>
<td><p><span data-ttu-id="1a594-128">Indique qu'à partir d'une transaction, vous ne pouvez pas voir les modifications des autres transactions, mais qu'une nouvelle requête peut extraire de nouveaux objets <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a594-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a594-129"><strong>à adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-130">1048576</span><span class="sxs-lookup"><span data-stu-id="1a594-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="1a594-131">Indique que les transactions sont réalisées indépendamment d'autres transactions.</span><span class="sxs-lookup"><span data-stu-id="1a594-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a594-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="1a594-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="1a594-133">1048576</span><span class="sxs-lookup"><span data-stu-id="1a594-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="1a594-134">Identique à <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a594-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1a594-135">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1a594-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="1a594-136">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1a594-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a594-137">Constante</span><span class="sxs-lookup"><span data-stu-id="1a594-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a594-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="1a594-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a594-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="1a594-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a594-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="1a594-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a594-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="1a594-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a594-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="1a594-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a594-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="1a594-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a594-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="1a594-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a594-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="1a594-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a594-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="1a594-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

