---
title: PermissionEnum, énumération (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d4f6741bd6203dbdeffb364650b5e3550ea8b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287709"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="33bfa-102">PermissionEnum, énumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="33bfa-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="33bfa-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33bfa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33bfa-104">Cette énumération est utilisée avec la propriété **Permissions** pour spécifier le type d'autorisations.</span><span class="sxs-lookup"><span data-stu-id="33bfa-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33bfa-105">Nom</span><span class="sxs-lookup"><span data-stu-id="33bfa-105">Name</span></span></p></th>
<th><p><span data-ttu-id="33bfa-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="33bfa-106">Value</span></span></p></th>
<th><p><span data-ttu-id="33bfa-107">Description</span><span class="sxs-lookup"><span data-stu-id="33bfa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="33bfa-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="33bfa-109">0,1</span><span class="sxs-lookup"><span data-stu-id="33bfa-109">1</span></span></p></td>
<td><p><span data-ttu-id="33bfa-110">L'utilisateur peut créer des documents (non valide pour les objets Document).</span><span class="sxs-lookup"><span data-stu-id="33bfa-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33bfa-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="33bfa-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="33bfa-112">8bits</span><span class="sxs-lookup"><span data-stu-id="33bfa-112">8</span></span></p></td>
<td><p><span data-ttu-id="33bfa-113">L'utilisateur peut répliquer une base de données et modifier le mot de passe de la base de données (non valide pour les objets Document).</span><span class="sxs-lookup"><span data-stu-id="33bfa-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="33bfa-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="33bfa-115">0,1</span><span class="sxs-lookup"><span data-stu-id="33bfa-115">1</span></span></p></td>
<td><p><span data-ttu-id="33bfa-p101">L'utilisateur peut créer des bases de données. Cette option est valide uniquement sur le conteneur de bases de données du fichier de groupe de travail (Systen.mdw). Cette constante n'est pas valide pour les objets Document.</span><span class="sxs-lookup"><span data-stu-id="33bfa-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33bfa-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="33bfa-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="33bfa-120">4</span><span class="sxs-lookup"><span data-stu-id="33bfa-120">4</span></span></p></td>
<td><p><span data-ttu-id="33bfa-121">L'utilisateur dispose d'un accès en mode exclusif à la base de données.</span><span class="sxs-lookup"><span data-stu-id="33bfa-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="33bfa-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="33bfa-123">n°2</span><span class="sxs-lookup"><span data-stu-id="33bfa-123">2</span></span></p></td>
<td><p><span data-ttu-id="33bfa-124">L'utilisateur peut ouvrir la base de données.</span><span class="sxs-lookup"><span data-stu-id="33bfa-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33bfa-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="33bfa-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="33bfa-126">65536</span><span class="sxs-lookup"><span data-stu-id="33bfa-126">65536</span></span></p></td>
<td><p><span data-ttu-id="33bfa-127">L'utilisateur peut supprimer l'objet.</span><span class="sxs-lookup"><span data-stu-id="33bfa-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="33bfa-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="33bfa-129">128</span><span class="sxs-lookup"><span data-stu-id="33bfa-129">128</span></span></p></td>
<td><p><span data-ttu-id="33bfa-130">L'utilisateur peut supprimer des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="33bfa-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33bfa-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="33bfa-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="33bfa-132">1048575</span><span class="sxs-lookup"><span data-stu-id="33bfa-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="33bfa-133">L'utilisateur dispose d'un accès complet à l'objet.</span><span class="sxs-lookup"><span data-stu-id="33bfa-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="33bfa-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="33bfa-135">32</span><span class="sxs-lookup"><span data-stu-id="33bfa-135">32</span></span></p></td>
<td><p><span data-ttu-id="33bfa-136">L'utilisateur peut ajouter des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="33bfa-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33bfa-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="33bfa-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="33bfa-138">0</span><span class="sxs-lookup"><span data-stu-id="33bfa-138">0</span></span></p></td>
<td><p><span data-ttu-id="33bfa-139">L'utilisateur n'a pas accès à l'objet (non valide pour les objets Document).</span><span class="sxs-lookup"><span data-stu-id="33bfa-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="33bfa-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="33bfa-141">4</span><span class="sxs-lookup"><span data-stu-id="33bfa-141">4</span></span></p></td>
<td><p><span data-ttu-id="33bfa-142">L'utilisateur peut lire la définition de table, notamment les informations d'index et de colonne.</span><span class="sxs-lookup"><span data-stu-id="33bfa-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33bfa-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="33bfa-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="33bfa-144">131072</span><span class="sxs-lookup"><span data-stu-id="33bfa-144">131072</span></span></p></td>
<td><p><span data-ttu-id="33bfa-145">L'utilisateur peut lire les informations sur la sécurité de l'objet.</span><span class="sxs-lookup"><span data-stu-id="33bfa-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="33bfa-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="33bfa-147">64</span><span class="sxs-lookup"><span data-stu-id="33bfa-147">64</span></span></p></td>
<td><p><span data-ttu-id="33bfa-148">L'utilisateur peut modifier des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="33bfa-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33bfa-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="33bfa-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="33bfa-150">vingtaine</span><span class="sxs-lookup"><span data-stu-id="33bfa-150">20</span></span></p></td>
<td><p><span data-ttu-id="33bfa-151">L'utilisateur peut récupérer des données de l'objet Document.</span><span class="sxs-lookup"><span data-stu-id="33bfa-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="33bfa-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="33bfa-153">65548</span><span class="sxs-lookup"><span data-stu-id="33bfa-153">65548</span></span></p></td>
<td><p><span data-ttu-id="33bfa-154">L'utilisateur peut modifier ou supprimer la définition de table, notamment les informations d'index et de colonne.</span><span class="sxs-lookup"><span data-stu-id="33bfa-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33bfa-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="33bfa-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="33bfa-156">524288</span><span class="sxs-lookup"><span data-stu-id="33bfa-156">524288</span></span></p></td>
<td><p><span data-ttu-id="33bfa-157">L'utilisateur peut modifier la définition de la propriété Propriétaire.</span><span class="sxs-lookup"><span data-stu-id="33bfa-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33bfa-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="33bfa-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="33bfa-159">262144</span><span class="sxs-lookup"><span data-stu-id="33bfa-159">262144</span></span></p></td>
<td><p><span data-ttu-id="33bfa-160">L'utilisateur peut modifier les autorisations d'accès.</span><span class="sxs-lookup"><span data-stu-id="33bfa-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

