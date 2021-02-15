---
title: LockTypeEnum (référence de base de données de bureau Access)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4b9dc49e647bdcd3123ade065da0c74538c9a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289863"
---
# <a name="locktypeenum"></a><span data-ttu-id="66791-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="66791-102">LockTypeEnum</span></span>

<span data-ttu-id="66791-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66791-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66791-104">Spécifie le type de verrouillage appliqué aux enregistrements pendant l'édition.</span><span class="sxs-lookup"><span data-stu-id="66791-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66791-105">Constante</span><span class="sxs-lookup"><span data-stu-id="66791-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="66791-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="66791-106">Value</span></span></p></th>
<th><p><span data-ttu-id="66791-107">Description</span><span class="sxs-lookup"><span data-stu-id="66791-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66791-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="66791-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="66791-109">4 </span><span class="sxs-lookup"><span data-stu-id="66791-109">4</span></span></p></td>
<td><p><span data-ttu-id="66791-p101">Indique des mises à jour par lots optimistes. Obligatoire pour le mode de mise à jour par lots.</span><span class="sxs-lookup"><span data-stu-id="66791-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66791-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="66791-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="66791-113">3 </span><span class="sxs-lookup"><span data-stu-id="66791-113">3</span></span></p></td>
<td><p><span data-ttu-id="66791-p102">Indique un verrouillage optimiste, enregistrement par enregistrement. Le fournisseur applique ce type de verrouillage lorsque vous faites appel à la méthode <a href="update-method-ado.md">Update</a>.</span><span class="sxs-lookup"><span data-stu-id="66791-p102">Indicates optimistic locking, record by record. The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66791-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="66791-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="66791-117">2 </span><span class="sxs-lookup"><span data-stu-id="66791-117">2</span></span></p></td>
<td><p><span data-ttu-id="66791-p103">Indique un verrouillage pessimiste, enregistrement par enregistrement. Le fournisseur fait en sorte que l'édition des enregistrements réussisse, en général en verrouillant les enregistrements à la source de données immédiatement après édition.</span><span class="sxs-lookup"><span data-stu-id="66791-p103">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66791-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="66791-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="66791-121">1 </span><span class="sxs-lookup"><span data-stu-id="66791-121">1</span></span></p></td>
<td><p><span data-ttu-id="66791-p104">Indique des enregistrements en lecture seule. Vous ne pouvez pas modifier les données.</span><span class="sxs-lookup"><span data-stu-id="66791-p104">Indicates read-only records. You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66791-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="66791-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="66791-125">-1</span><span class="sxs-lookup"><span data-stu-id="66791-125">-1</span></span></p></td>
<td><p><span data-ttu-id="66791-p105">Ne spécifie pas de type de verrouillage. Un clone est créé avec le même type de verrouillage que l'original.</span><span class="sxs-lookup"><span data-stu-id="66791-p105">Does not specify a type of lock. For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="66791-128">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="66791-128">ADO/WFC equivalent</span></span>

<span data-ttu-id="66791-129">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="66791-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66791-130">Constante</span><span class="sxs-lookup"><span data-stu-id="66791-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66791-131">AdoEnums.LockType.BATINTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="66791-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66791-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="66791-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66791-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="66791-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66791-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="66791-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66791-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="66791-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

