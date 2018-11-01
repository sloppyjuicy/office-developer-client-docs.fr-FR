---
title: RightsEnum (référence de base de données du bureau Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 535c80bf5cd3dbfecae0e004082ce20d01c31fde
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877386"
---
# <a name="rightsenum"></a><span data-ttu-id="75e5a-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="75e5a-102">RightsEnum</span></span>

<span data-ttu-id="75e5a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75e5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75e5a-104">Spécifie les droits ou autorisations d'un groupe ou d'un utilisateur sur un objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75e5a-105">Constante</span><span class="sxs-lookup"><span data-stu-id="75e5a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="75e5a-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="75e5a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="75e5a-107">Description</span><span class="sxs-lookup"><span data-stu-id="75e5a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-109">16384</span><span class="sxs-lookup"><span data-stu-id="75e5a-109">16384</span></span><br />
<span data-ttu-id="75e5a-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-111">L'utilisateur ou le groupe a l'autorisation de créer de nouveaux objets de ce type.</span><span class="sxs-lookup"><span data-stu-id="75e5a-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-113">65536</span><span class="sxs-lookup"><span data-stu-id="75e5a-113">65536</span></span><br />
<span data-ttu-id="75e5a-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-p101">L'utilisateur ou le groupe a l'autorisation de supprimer des données d'un objet. Pour des objets de type <strong>Table</strong> par exemple, l'utilisateur a l'autorisation de supprimer des valeurs de données dans des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="75e5a-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-118">256</span><span class="sxs-lookup"><span data-stu-id="75e5a-118">256</span></span><br />
<span data-ttu-id="75e5a-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="75e5a-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-p102">L'utilisateur ou le groupe a l'autorisation de supprimer des objets du catalogue. Par exemple, il peut supprimer un objet <strong>Table</strong> à l'aide de la commande DROP TABLE SQL.</span><span class="sxs-lookup"><span data-stu-id="75e5a-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-123">512</span><span class="sxs-lookup"><span data-stu-id="75e5a-123">512</span></span><br />
<span data-ttu-id="75e5a-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="75e5a-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-125">L'utilisateur ou le groupe a l'autorisation d'accéder à l'objet en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="75e5a-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-127">536870912</span><span class="sxs-lookup"><span data-stu-id="75e5a-127">536870912</span></span><br />
<span data-ttu-id="75e5a-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-129">L'utilisateur ou le groupe a l'autorisation d'exécuter l'objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-131">268435456</span><span class="sxs-lookup"><span data-stu-id="75e5a-131">268435456</span></span><br />
<span data-ttu-id="75e5a-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-133">L'utilisateur ou le groupe dispose d'autorisations complètes sur l'objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-135">32768</span><span class="sxs-lookup"><span data-stu-id="75e5a-135">32768</span></span><br />
<span data-ttu-id="75e5a-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-p103">L'utilisateur ou le groupe a l'autorisation d'insérer l'objet. Pour des objets de type <strong>Table</strong>, l'utilisateur a l'autorisation d'insérer des données dans la table.</span><span class="sxs-lookup"><span data-stu-id="75e5a-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-p104">L'utilisateur ou le groupe dispose du nombre maximal d'autorisations admises par le fournisseur. Les autorisations spécifiques dépendent du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="75e5a-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-144">0</span><span class="sxs-lookup"><span data-stu-id="75e5a-144">0</span></span></p></td>
<td><p><span data-ttu-id="75e5a-145">L'utilisateur ou le groupe n'a aucune autorisation pour l'objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="75e5a-147">-2147483648</span></span><br />
<span data-ttu-id="75e5a-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-p105">L’utilisateur ou le groupe a l’autorisation de lire l’objet. Pour des objets de type <a href="table-object-adox.md">Table</a>, l’utilisateur est autorisé à lire les données de la table.</span><span class="sxs-lookup"><span data-stu-id="75e5a-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-152">1024</span><span class="sxs-lookup"><span data-stu-id="75e5a-152">1024</span></span><br />
<span data-ttu-id="75e5a-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="75e5a-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-154">L'utilisateur ou le groupe a l'autorisation de lire la conception de l'objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-156">131072</span><span class="sxs-lookup"><span data-stu-id="75e5a-156">131072</span></span><br />
<span data-ttu-id="75e5a-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-158">L'utilisateur ou le groupe peut afficher mais non modifier les autorisations spécifiques liées à un objet dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="75e5a-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-160">8192</span><span class="sxs-lookup"><span data-stu-id="75e5a-160">8192</span></span><br />
<span data-ttu-id="75e5a-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-162">L'utilisateur ou le groupe a l'autorisation de faire référence à l'objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="75e5a-164">1073741824</span></span><br />
<span data-ttu-id="75e5a-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-p106">L'utilisateur ou le groupe a l'autorisation de mettre à jour l'objet. Pour des objets de type <strong>Table</strong>, l'utilisateur est autorisé à mettre à jour les données de la table.</span><span class="sxs-lookup"><span data-stu-id="75e5a-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-169">4096</span><span class="sxs-lookup"><span data-stu-id="75e5a-169">4096</span></span><br />
<span data-ttu-id="75e5a-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-171">L'utilisateur ou le groupe est autorisé à octroyer des autorisations sur l'objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-173">2048</span><span class="sxs-lookup"><span data-stu-id="75e5a-173">2048</span></span><br />
<span data-ttu-id="75e5a-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="75e5a-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-175">L'utilisateur ou le groupe a l'autorisation de modifier la conception de l'objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-177">524288</span><span class="sxs-lookup"><span data-stu-id="75e5a-177">524288</span></span><br />
<span data-ttu-id="75e5a-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-179">L'utilisateur ou le groupe a l'autorisation de modifier le propriétaire de l'objet.</span><span class="sxs-lookup"><span data-stu-id="75e5a-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-181">262144</span><span class="sxs-lookup"><span data-stu-id="75e5a-181">262144</span></span><br />
<span data-ttu-id="75e5a-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="75e5a-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-183">L'utilisateur ou le groupe peut modifier les autorisations spécifiques liées à un objet dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="75e5a-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

