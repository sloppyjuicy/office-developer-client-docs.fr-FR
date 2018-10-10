---
title: RecordStatusEnum (référence de base de données du bureau Access)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88929ced56583316c42f2d5195054e51e98a1d5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470486"
---
# <a name="recordstatusenum"></a><span data-ttu-id="2213a-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="2213a-102">RecordStatusEnum</span></span>


<span data-ttu-id="2213a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2213a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2213a-104">Spécifie l'état d'un enregistrement en cas de mise à jour par lots et autres opérations globales de ce type.</span><span class="sxs-lookup"><span data-stu-id="2213a-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2213a-105">Constante</span><span class="sxs-lookup"><span data-stu-id="2213a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2213a-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="2213a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2213a-107">Description</span><span class="sxs-lookup"><span data-stu-id="2213a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2213a-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-109">0 x 100</span><span class="sxs-lookup"><span data-stu-id="2213a-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="2213a-110">Indique que l'enregistrement n'a pas été sauvegardé car l'opération a été annulée.</span><span class="sxs-lookup"><span data-stu-id="2213a-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-112">0 x 400</span><span class="sxs-lookup"><span data-stu-id="2213a-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="2213a-113">Indique que le nouvel enregistrement n'a pas été sauvegardé car l'enregistrement existant était verrouillé.</span><span class="sxs-lookup"><span data-stu-id="2213a-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-115">0 x 800</span><span class="sxs-lookup"><span data-stu-id="2213a-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="2213a-116">Indique que l'enregistrement n'a pas été sauvegardé car une concurrence optimiste était en cours.</span><span class="sxs-lookup"><span data-stu-id="2213a-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-118">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="2213a-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="2213a-119">Indique que l'enregistrement a déjà été supprimé de la source de données.</span><span class="sxs-lookup"><span data-stu-id="2213a-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-121">0 x 4</span><span class="sxs-lookup"><span data-stu-id="2213a-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="2213a-122">Indique que l'enregistrement a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="2213a-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-124">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="2213a-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="2213a-125">Indique que l'enregistrement n'a pas été sauvegardé car l'utilisateur n'a pas respecté les contraintes d'intégrité.</span><span class="sxs-lookup"><span data-stu-id="2213a-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-127">0 x 10</span><span class="sxs-lookup"><span data-stu-id="2213a-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="2213a-128">Indique que l'enregistrement n'a pas été sauvegardé car son signet n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2213a-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-130">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="2213a-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="2213a-131">Indique que l'enregistrement n'a pas été sauvegardé car il existait trop de modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="2213a-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-133">0 x 2</span><span class="sxs-lookup"><span data-stu-id="2213a-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="2213a-134">Indique que l'enregistrement a été modifié.</span><span class="sxs-lookup"><span data-stu-id="2213a-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-136">0 x 40</span><span class="sxs-lookup"><span data-stu-id="2213a-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="2213a-137">Indique que l'enregistrement n'a pas été sauvegardé car il aurait affecté plusieurs enregistrements.</span><span class="sxs-lookup"><span data-stu-id="2213a-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-139">0 x 1</span><span class="sxs-lookup"><span data-stu-id="2213a-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="2213a-140">Indique qu'il s'agit d'un nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2213a-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-142">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="2213a-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="2213a-143">Indique que l'enregistrement n'a pas été sauvegardé en raison d'un conflit avec un objet de stockage ouvert.</span><span class="sxs-lookup"><span data-stu-id="2213a-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-145">0</span><span class="sxs-lookup"><span data-stu-id="2213a-145">0</span></span></p></td>
<td><p><span data-ttu-id="2213a-146">Indique que l'enregistrement a été mis à jour avec succès.</span><span class="sxs-lookup"><span data-stu-id="2213a-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-148">0 x 8000</span><span class="sxs-lookup"><span data-stu-id="2213a-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="2213a-149">Indique que l'enregistrement n'a pas été sauvegardé car l'ordinateur manque de mémoire.</span><span class="sxs-lookup"><span data-stu-id="2213a-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-151">0 x 80</span><span class="sxs-lookup"><span data-stu-id="2213a-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="2213a-152">Indique que l'enregistrement n'a pas été sauvegardé car il fait référence à une insertion en attente.</span><span class="sxs-lookup"><span data-stu-id="2213a-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-154">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="2213a-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="2213a-155">Indique que l'enregistrement n'a pas été sauvegardé car l'utilisateur ne dispose pas des autorisations suffisantes.</span><span class="sxs-lookup"><span data-stu-id="2213a-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-157">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="2213a-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="2213a-158">Indique que l'enregistrement n'a pas été sauvegardé car il ne respecte pas la structure de la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="2213a-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="2213a-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="2213a-160">0 x 8</span><span class="sxs-lookup"><span data-stu-id="2213a-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="2213a-161">Indique que l'enregistrement n'a pas été modifié.</span><span class="sxs-lookup"><span data-stu-id="2213a-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2213a-162">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="2213a-162">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="2213a-163">AdoEnums.RecordStatus.</span><span class="sxs-lookup"><span data-stu-id="2213a-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="2213a-164">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2213a-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2213a-165">Constante</span><span class="sxs-lookup"><span data-stu-id="2213a-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2213a-166">AdoEnums.RecordStatus.CANCELED</span><span class="sxs-lookup"><span data-stu-id="2213a-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-167">AdoEnums.RecordStatus.CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="2213a-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="2213a-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-169">AdoEnums.RecordStatus.DBDELETED</span><span class="sxs-lookup"><span data-stu-id="2213a-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-170">AdoEnums.RecordStatus.DELETED</span><span class="sxs-lookup"><span data-stu-id="2213a-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="2213a-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-172">AdoEnums.RecordStatus.INVALID</span><span class="sxs-lookup"><span data-stu-id="2213a-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="2213a-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-174">AdoEnums.RecordStatus.MODIFIED</span><span class="sxs-lookup"><span data-stu-id="2213a-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="2213a-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-176">AdoEnums.RecordStatus.NEW</span><span class="sxs-lookup"><span data-stu-id="2213a-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-177">AdoEnums.RecordStatus.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="2213a-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-178">AdoEnums.RecordStatus.OK</span><span class="sxs-lookup"><span data-stu-id="2213a-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-179">AdoEnums.RecordStatus.OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="2213a-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-180">AdoEnums.RecordStatus.PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="2213a-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="2213a-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2213a-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="2213a-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2213a-183">AdoEnums.RecordStatus.UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="2213a-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

