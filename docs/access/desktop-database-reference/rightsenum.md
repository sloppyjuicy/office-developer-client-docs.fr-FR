---
title: RightsEnum (référence de base de données du bureau Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 40cd7f789461e5b354186c2d5b8f81ec18344435
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861980"
---
# <a name="rightsenum"></a><span data-ttu-id="4d7f5-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="4d7f5-102">RightsEnum</span></span>

<span data-ttu-id="4d7f5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d7f5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4d7f5-104">Spécifie les droits ou autorisations d'un groupe ou d'un utilisateur sur un objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d7f5-105">Constante</span><span class="sxs-lookup"><span data-stu-id="4d7f5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4d7f5-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d7f5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4d7f5-107">Description</span><span class="sxs-lookup"><span data-stu-id="4d7f5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-109">16384</span><span class="sxs-lookup"><span data-stu-id="4d7f5-109">16384</span></span><br />
<span data-ttu-id="4d7f5-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-111">L'utilisateur ou le groupe a l'autorisation de créer de nouveaux objets de ce type.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-113">65536</span><span class="sxs-lookup"><span data-stu-id="4d7f5-113">65536</span></span><br />
<span data-ttu-id="4d7f5-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-p101">L'utilisateur ou le groupe a l'autorisation de supprimer des données d'un objet. Pour des objets de type <strong>Table</strong> par exemple, l'utilisateur a l'autorisation de supprimer des valeurs de données dans des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-118">256</span><span class="sxs-lookup"><span data-stu-id="4d7f5-118">256</span></span><br />
<span data-ttu-id="4d7f5-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-p102">L'utilisateur ou le groupe a l'autorisation de supprimer des objets du catalogue. Par exemple, il peut supprimer un objet <strong>Table</strong> à l'aide de la commande DROP TABLE SQL.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-123">512</span><span class="sxs-lookup"><span data-stu-id="4d7f5-123">512</span></span><br />
<span data-ttu-id="4d7f5-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-125">L'utilisateur ou le groupe a l'autorisation d'accéder à l'objet en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-127">536870912</span><span class="sxs-lookup"><span data-stu-id="4d7f5-127">536870912</span></span><br />
<span data-ttu-id="4d7f5-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-129">L'utilisateur ou le groupe a l'autorisation d'exécuter l'objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-131">268435456</span><span class="sxs-lookup"><span data-stu-id="4d7f5-131">268435456</span></span><br />
<span data-ttu-id="4d7f5-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-133">L'utilisateur ou le groupe dispose d'autorisations complètes sur l'objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-135">32768</span><span class="sxs-lookup"><span data-stu-id="4d7f5-135">32768</span></span><br />
<span data-ttu-id="4d7f5-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-p103">L'utilisateur ou le groupe a l'autorisation d'insérer l'objet. Pour des objets de type <strong>Table</strong>, l'utilisateur a l'autorisation d'insérer des données dans la table.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-p104">L'utilisateur ou le groupe dispose du nombre maximal d'autorisations admises par le fournisseur. Les autorisations spécifiques dépendent du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-144">0</span><span class="sxs-lookup"><span data-stu-id="4d7f5-144">0</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-145">L'utilisateur ou le groupe n'a aucune autorisation pour l'objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="4d7f5-147">-2147483648</span></span><br />
<span data-ttu-id="4d7f5-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-p105">L’utilisateur ou le groupe a l’autorisation de lire l’objet. Pour des objets de type <a href="table-object-adox.md">Table</a>, l’utilisateur est autorisé à lire les données de la table.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-152">1024</span><span class="sxs-lookup"><span data-stu-id="4d7f5-152">1024</span></span><br />
<span data-ttu-id="4d7f5-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-154">L'utilisateur ou le groupe a l'autorisation de lire la conception de l'objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-156">131072</span><span class="sxs-lookup"><span data-stu-id="4d7f5-156">131072</span></span><br />
<span data-ttu-id="4d7f5-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-158">L'utilisateur ou le groupe peut afficher mais non modifier les autorisations spécifiques liées à un objet dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-160">8192</span><span class="sxs-lookup"><span data-stu-id="4d7f5-160">8192</span></span><br />
<span data-ttu-id="4d7f5-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-162">L'utilisateur ou le groupe a l'autorisation de faire référence à l'objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="4d7f5-164">1073741824</span></span><br />
<span data-ttu-id="4d7f5-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-p106">L'utilisateur ou le groupe a l'autorisation de mettre à jour l'objet. Pour des objets de type <strong>Table</strong>, l'utilisateur est autorisé à mettre à jour les données de la table.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-169">4096</span><span class="sxs-lookup"><span data-stu-id="4d7f5-169">4096</span></span><br />
<span data-ttu-id="4d7f5-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-171">L'utilisateur ou le groupe est autorisé à octroyer des autorisations sur l'objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-173">2048</span><span class="sxs-lookup"><span data-stu-id="4d7f5-173">2048</span></span><br />
<span data-ttu-id="4d7f5-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-175">L'utilisateur ou le groupe a l'autorisation de modifier la conception de l'objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d7f5-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-177">524288</span><span class="sxs-lookup"><span data-stu-id="4d7f5-177">524288</span></span><br />
<span data-ttu-id="4d7f5-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-179">L'utilisateur ou le groupe a l'autorisation de modifier le propriétaire de l'objet.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d7f5-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="4d7f5-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="4d7f5-181">262144</span><span class="sxs-lookup"><span data-stu-id="4d7f5-181">262144</span></span><br />
<span data-ttu-id="4d7f5-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="4d7f5-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="4d7f5-183">L'utilisateur ou le groupe peut modifier les autorisations spécifiques liées à un objet dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="4d7f5-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

