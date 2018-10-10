---
title: FilterGroupEnum (référence de base de données du bureau Access)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd89cd0b261d8573dfd7c0047cca7890235ffb2b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469124"
---
# <a name="filtergroupenum"></a><span data-ttu-id="f9255-102">FilterGroupEnum</span><span class="sxs-lookup"><span data-stu-id="f9255-102">FilterGroupEnum</span></span>


<span data-ttu-id="f9255-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9255-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f9255-104">Spécifie le groupe d'enregistrements à filtrer depuis un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f9255-104">Specifies the group of records to be filtered from a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9255-105">Constant</span><span class="sxs-lookup"><span data-stu-id="f9255-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f9255-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9255-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f9255-107">Description</span><span class="sxs-lookup"><span data-stu-id="f9255-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9255-108"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="f9255-108"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="f9255-109">2</span><span class="sxs-lookup"><span data-stu-id="f9255-109">2</span></span></p></td>
<td><p><span data-ttu-id="f9255-110">Filtres pour ne visualiser que les enregistrements affectés par le dernier appel <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a> ou <a href="cancelbatch-method-ado.md">CancelBatch</a>.</span><span class="sxs-lookup"><span data-stu-id="f9255-110">Filters for viewing only records affected by the last <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>, or <a href="cancelbatch-method-ado.md">CancelBatch</a> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9255-111"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="f9255-111"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="f9255-112">5</span><span class="sxs-lookup"><span data-stu-id="f9255-112">5</span></span></p></td>
<td><p><span data-ttu-id="f9255-113">Filtres pour visualiser les enregistrements qui ont échoué à la dernière mise à jour par lots.</span><span class="sxs-lookup"><span data-stu-id="f9255-113">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9255-114"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="f9255-114"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="f9255-115">3</span><span class="sxs-lookup"><span data-stu-id="f9255-115">3</span></span></p></td>
<td><p><span data-ttu-id="f9255-116">Filtres pour visualiser les enregistrements se trouvant en mémoire cache  —- en fait, les résultats de la dernière extraction d'enregistrements de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f9255-116">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9255-117"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="f9255-117"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="f9255-118">0</span><span class="sxs-lookup"><span data-stu-id="f9255-118">0</span></span></p></td>
<td><p><span data-ttu-id="f9255-119">Supprime le filtre en cours et restaure tous les enregistrements pour visualisation.</span><span class="sxs-lookup"><span data-stu-id="f9255-119">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9255-120"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="f9255-120"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="f9255-121">1</span><span class="sxs-lookup"><span data-stu-id="f9255-121">1</span></span></p></td>
<td><p><span data-ttu-id="f9255-p101">Filtres permettant de ne visualiser que les enregistrements modifiés mais pas encore envoyés au serveur. Applicables seulement en mode de mise à jour par lots.</span><span class="sxs-lookup"><span data-stu-id="f9255-p101">Filters for viewing only records that have changed but have not yet been sent to the server. Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f9255-124">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="f9255-124">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="f9255-125">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f9255-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9255-126">Constante</span><span class="sxs-lookup"><span data-stu-id="f9255-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9255-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="f9255-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9255-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="f9255-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9255-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="f9255-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9255-130">AdoEnums.FilterGroup.NONE</span><span class="sxs-lookup"><span data-stu-id="f9255-130">AdoEnums.FilterGroup.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9255-131">AdoEnums.FilterGroup.PENDINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="f9255-131">AdoEnums.FilterGroup.PENDINGRECORDS</span></span></p></td>
</tr>
</tbody>
</table>

