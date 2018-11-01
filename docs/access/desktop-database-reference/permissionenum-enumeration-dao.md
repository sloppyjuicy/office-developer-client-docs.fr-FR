---
title: PermissionEnum Enumeration (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3583737eebc881ed5462fe76b6e4a37ad25a8f3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875223"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="b97e1-102">PermissionEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="b97e1-102">PermissionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="b97e1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b97e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b97e1-104">Cette énumération est utilisée avec la propriété **Permissions** pour spécifier le type d'autorisations.</span><span class="sxs-lookup"><span data-stu-id="b97e1-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b97e1-105">Nom</span><span class="sxs-lookup"><span data-stu-id="b97e1-105">Name</span></span></p></th>
<th><p><span data-ttu-id="b97e1-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97e1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b97e1-107">Description</span><span class="sxs-lookup"><span data-stu-id="b97e1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="b97e1-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="b97e1-109">1</span><span class="sxs-lookup"><span data-stu-id="b97e1-109">1</span></span></p></td>
<td><p><span data-ttu-id="b97e1-110">L'utilisateur peut créer des documents (non valide pour les objets Document).</span><span class="sxs-lookup"><span data-stu-id="b97e1-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b97e1-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="b97e1-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="b97e1-112">8</span><span class="sxs-lookup"><span data-stu-id="b97e1-112">8</span></span></p></td>
<td><p><span data-ttu-id="b97e1-113">L'utilisateur peut répliquer une base de données et modifier le mot de passe de la base de données (non valide pour les objets Document).</span><span class="sxs-lookup"><span data-stu-id="b97e1-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="b97e1-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="b97e1-115">1</span><span class="sxs-lookup"><span data-stu-id="b97e1-115">1</span></span></p></td>
<td><p><span data-ttu-id="b97e1-p101">L'utilisateur peut créer des bases de données. Cette option est valide uniquement sur le conteneur de bases de données du fichier de groupe de travail (Systen.mdw). Cette constante n'est pas valide pour les objets Document.</span><span class="sxs-lookup"><span data-stu-id="b97e1-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b97e1-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="b97e1-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="b97e1-120">4</span><span class="sxs-lookup"><span data-stu-id="b97e1-120">4</span></span></p></td>
<td><p><span data-ttu-id="b97e1-121">L'utilisateur dispose d'un accès en mode exclusif à la base de données.</span><span class="sxs-lookup"><span data-stu-id="b97e1-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="b97e1-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="b97e1-123">2</span><span class="sxs-lookup"><span data-stu-id="b97e1-123">2</span></span></p></td>
<td><p><span data-ttu-id="b97e1-124">L'utilisateur peut ouvrir la base de données.</span><span class="sxs-lookup"><span data-stu-id="b97e1-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b97e1-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="b97e1-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="b97e1-126">65536</span><span class="sxs-lookup"><span data-stu-id="b97e1-126">65536</span></span></p></td>
<td><p><span data-ttu-id="b97e1-127">L'utilisateur peut supprimer l'objet.</span><span class="sxs-lookup"><span data-stu-id="b97e1-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="b97e1-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="b97e1-129">128</span><span class="sxs-lookup"><span data-stu-id="b97e1-129">128</span></span></p></td>
<td><p><span data-ttu-id="b97e1-130">L'utilisateur peut supprimer des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="b97e1-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b97e1-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="b97e1-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="b97e1-132">1048575</span><span class="sxs-lookup"><span data-stu-id="b97e1-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="b97e1-133">L'utilisateur dispose d'un accès complet à l'objet.</span><span class="sxs-lookup"><span data-stu-id="b97e1-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="b97e1-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="b97e1-135">32</span><span class="sxs-lookup"><span data-stu-id="b97e1-135">32</span></span></p></td>
<td><p><span data-ttu-id="b97e1-136">L'utilisateur peut ajouter des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="b97e1-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b97e1-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="b97e1-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="b97e1-138">0</span><span class="sxs-lookup"><span data-stu-id="b97e1-138">0</span></span></p></td>
<td><p><span data-ttu-id="b97e1-139">L'utilisateur n'a pas accès à l'objet (non valide pour les objets Document).</span><span class="sxs-lookup"><span data-stu-id="b97e1-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="b97e1-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="b97e1-141">4</span><span class="sxs-lookup"><span data-stu-id="b97e1-141">4</span></span></p></td>
<td><p><span data-ttu-id="b97e1-142">L'utilisateur peut lire la définition de table, notamment les informations d'index et de colonne.</span><span class="sxs-lookup"><span data-stu-id="b97e1-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b97e1-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="b97e1-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="b97e1-144">131072</span><span class="sxs-lookup"><span data-stu-id="b97e1-144">131072</span></span></p></td>
<td><p><span data-ttu-id="b97e1-145">L'utilisateur peut lire les informations sur la sécurité de l'objet.</span><span class="sxs-lookup"><span data-stu-id="b97e1-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="b97e1-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="b97e1-147">64</span><span class="sxs-lookup"><span data-stu-id="b97e1-147">64</span></span></p></td>
<td><p><span data-ttu-id="b97e1-148">L'utilisateur peut modifier des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="b97e1-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b97e1-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="b97e1-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="b97e1-150">20</span><span class="sxs-lookup"><span data-stu-id="b97e1-150">20</span></span></p></td>
<td><p><span data-ttu-id="b97e1-151">L'utilisateur peut récupérer des données de l'objet Document.</span><span class="sxs-lookup"><span data-stu-id="b97e1-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-152">valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b97e1-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="b97e1-153">65548</span><span class="sxs-lookup"><span data-stu-id="b97e1-153">65548</span></span></p></td>
<td><p><span data-ttu-id="b97e1-154">L'utilisateur peut modifier ou supprimer la définition de table, notamment les informations d'index et de colonne.</span><span class="sxs-lookup"><span data-stu-id="b97e1-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b97e1-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="b97e1-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="b97e1-156">524288</span><span class="sxs-lookup"><span data-stu-id="b97e1-156">524288</span></span></p></td>
<td><p><span data-ttu-id="b97e1-157">L'utilisateur peut modifier la définition de la propriété Propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b97e1-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b97e1-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="b97e1-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="b97e1-159">262144</span><span class="sxs-lookup"><span data-stu-id="b97e1-159">262144</span></span></p></td>
<td><p><span data-ttu-id="b97e1-160">L'utilisateur peut modifier les autorisations d'accès.</span><span class="sxs-lookup"><span data-stu-id="b97e1-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

