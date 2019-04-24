---
title: RightsEnum (référence de base de données de bureau Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306488"
---
# <a name="rightsenum"></a><span data-ttu-id="3cc1d-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="3cc1d-102">RightsEnum</span></span>

<span data-ttu-id="3cc1d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cc1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cc1d-104">Spécifie les droits ou autorisations d'un groupe ou d'un utilisateur sur un objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cc1d-105">Constante</span><span class="sxs-lookup"><span data-stu-id="3cc1d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3cc1d-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cc1d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3cc1d-107">Description</span><span class="sxs-lookup"><span data-stu-id="3cc1d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-109">16384</span><span class="sxs-lookup"><span data-stu-id="3cc1d-109">16384</span></span><br />
<span data-ttu-id="3cc1d-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-111">L'utilisateur ou le groupe a l'autorisation de créer de nouveaux objets de ce type.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-113">65536</span><span class="sxs-lookup"><span data-stu-id="3cc1d-113">65536</span></span><br />
<span data-ttu-id="3cc1d-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-p101">L'utilisateur ou le groupe a l'autorisation de supprimer des données d'un objet. Pour des objets de type <strong>Table</strong> par exemple, l'utilisateur a l'autorisation de supprimer des valeurs de données dans des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-118">256</span><span class="sxs-lookup"><span data-stu-id="3cc1d-118">256</span></span><br />
<span data-ttu-id="3cc1d-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-p102">L'utilisateur ou le groupe a l'autorisation de supprimer des objets du catalogue. Par exemple, il peut supprimer un objet <strong>Table</strong> à l'aide de la commande DROP TABLE SQL.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-123">512</span><span class="sxs-lookup"><span data-stu-id="3cc1d-123">512</span></span><br />
<span data-ttu-id="3cc1d-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-125">L'utilisateur ou le groupe a l'autorisation d'accéder à l'objet en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-127">536870912</span><span class="sxs-lookup"><span data-stu-id="3cc1d-127">536870912</span></span><br />
<span data-ttu-id="3cc1d-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-129">L'utilisateur ou le groupe a l'autorisation d'exécuter l'objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-131">268435456</span><span class="sxs-lookup"><span data-stu-id="3cc1d-131">268435456</span></span><br />
<span data-ttu-id="3cc1d-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-133">L'utilisateur ou le groupe dispose d'autorisations complètes sur l'objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-135">32768</span><span class="sxs-lookup"><span data-stu-id="3cc1d-135">32768</span></span><br />
<span data-ttu-id="3cc1d-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-p103">L'utilisateur ou le groupe a l'autorisation d'insérer l'objet. Pour des objets de type <strong>Table</strong>, l'utilisateur a l'autorisation d'insérer des données dans la table.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-141">L'utilisateur ou le groupe dispose du nombre maximal d'autorisations admises par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-141">The user or group has the maximum number of permissions allowed by the provider.</span></span> <span data-ttu-id="3cc1d-142">Les autorisations spécifiques dépendent du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-142">Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-144">0</span><span class="sxs-lookup"><span data-stu-id="3cc1d-144">0</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-145">L'utilisateur ou le groupe n'a aucune autorisation pour l'objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="3cc1d-147">-2147483648</span></span><br />
<span data-ttu-id="3cc1d-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-p105">L’utilisateur ou le groupe a l’autorisation de lire l’objet. Pour des objets de type <a href="table-object-adox.md">Table</a>, l’utilisateur est autorisé à lire les données de la table.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-152">1024</span><span class="sxs-lookup"><span data-stu-id="3cc1d-152">1024</span></span><br />
<span data-ttu-id="3cc1d-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-154">L'utilisateur ou le groupe a l'autorisation de lire la conception de l'objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-156">131072</span><span class="sxs-lookup"><span data-stu-id="3cc1d-156">131072</span></span><br />
<span data-ttu-id="3cc1d-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-158">L'utilisateur ou le groupe peut afficher mais non modifier les autorisations spécifiques liées à un objet dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-160">8192</span><span class="sxs-lookup"><span data-stu-id="3cc1d-160">8192</span></span><br />
<span data-ttu-id="3cc1d-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-162">L'utilisateur ou le groupe a l'autorisation de faire référence à l'objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="3cc1d-164">1073741824</span></span><br />
<span data-ttu-id="3cc1d-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-p106">L'utilisateur ou le groupe a l'autorisation de mettre à jour l'objet. Pour des objets de type <strong>Table</strong>, l'utilisateur est autorisé à mettre à jour les données de la table.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-169">4096</span><span class="sxs-lookup"><span data-stu-id="3cc1d-169">4096</span></span><br />
<span data-ttu-id="3cc1d-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-171">L'utilisateur ou le groupe est autorisé à octroyer des autorisations sur l'objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-173">2048</span><span class="sxs-lookup"><span data-stu-id="3cc1d-173">2048</span></span><br />
<span data-ttu-id="3cc1d-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-175">L'utilisateur ou le groupe a l'autorisation de modifier la conception de l'objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc1d-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-177">524288</span><span class="sxs-lookup"><span data-stu-id="3cc1d-177">524288</span></span><br />
<span data-ttu-id="3cc1d-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-179">L'utilisateur ou le groupe a l'autorisation de modifier le propriétaire de l'objet.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc1d-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="3cc1d-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc1d-181">262144</span><span class="sxs-lookup"><span data-stu-id="3cc1d-181">262144</span></span><br />
<span data-ttu-id="3cc1d-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="3cc1d-183">L'utilisateur ou le groupe peut modifier les autorisations spécifiques liées à un objet dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

