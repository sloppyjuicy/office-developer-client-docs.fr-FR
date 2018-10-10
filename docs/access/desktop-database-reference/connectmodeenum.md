---
title: ConnectModeEnum (référence de base de données du bureau Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b39fc42259a1906891b82bf9b9ef252997e6240
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471984"
---
# <a name="connectmodeenum"></a><span data-ttu-id="30d71-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="30d71-102">ConnectModeEnum</span></span>


<span data-ttu-id="30d71-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="30d71-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="30d71-104">Spécifie les autorisations disponibles pour modifier les données dans une [Connexion](connection-object-ado.md), en ouvrant un [Enregistrement](record-object-ado.md), ou en spécifiant des valeurs pour la propriété [Mode](mode-property-ado.md) de l' **Enregistrement** et des objets [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="30d71-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30d71-105">Constant</span><span class="sxs-lookup"><span data-stu-id="30d71-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="30d71-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="30d71-106">Value</span></span></p></th>
<th><p><span data-ttu-id="30d71-107">Description</span><span class="sxs-lookup"><span data-stu-id="30d71-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30d71-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-109">1</span><span class="sxs-lookup"><span data-stu-id="30d71-109">1</span></span></p></td>
<td><p><span data-ttu-id="30d71-110">Indique des autorisations en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="30d71-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30d71-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-112">3</span><span class="sxs-lookup"><span data-stu-id="30d71-112">3</span></span></p></td>
<td><p><span data-ttu-id="30d71-113">Indique des autorisations en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="30d71-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30d71-114"><strong>encore adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-115">0 x 400000</span><span class="sxs-lookup"><span data-stu-id="30d71-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="30d71-116">Utilisée conjointement avec les autres valeurs <em>*ShareDeny*</em> (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>ou <strong>adModeShareDenyRead</strong>) pour propager les restrictions de partage à tous les enregistrements secondaire de l' <strong>enregistrement</strong>actif.</span><span class="sxs-lookup"><span data-stu-id="30d71-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="30d71-117">Il n’a aucun effet si l' <strong>enregistrement</strong> n’a pas d’enfants.</span><span class="sxs-lookup"><span data-stu-id="30d71-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span> <span data-ttu-id="30d71-118">Une erreur d’exécution est générée si elle est utilisée avec <strong>adModeShareDenyNone</strong> .</span><span class="sxs-lookup"><span data-stu-id="30d71-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="30d71-119">Toutefois, il peut être utilisé avec <strong>adModeShareDenyNone</strong> lorsqu’il est associé avec d’autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="30d71-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="30d71-120">Par exemple, vous pouvez utiliser &quot; <strong>adModeRead</strong> ou <strong>adModeShareDenyNone</strong> ou <strong>encore adModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="30d71-120">For example, you can use &quot;<strong>adModeRead</strong> Or <strong>adModeShareDenyNone</strong> Or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30d71-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-122">16</span><span class="sxs-lookup"><span data-stu-id="30d71-122">16</span></span></p></td>
<td><p><span data-ttu-id="30d71-p102">Permet à d'autres utilisateurs d'ouvrir une connexion sans autorisations d'aucune sorte. L'accès en lecture et en écriture ne pourra être interdit.</span><span class="sxs-lookup"><span data-stu-id="30d71-p102">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30d71-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-126">4</span><span class="sxs-lookup"><span data-stu-id="30d71-126">4</span></span></p></td>
<td><p><span data-ttu-id="30d71-127">Empêche d'autres utilisateurs d'ouvrir une connexion sans autorisation de lecture.</span><span class="sxs-lookup"><span data-stu-id="30d71-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30d71-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-129">8</span><span class="sxs-lookup"><span data-stu-id="30d71-129">8</span></span></p></td>
<td><p><span data-ttu-id="30d71-130">Empêche d'autres utilisateurs d'ouvrir une connexion sans autorisation d'écriture.</span><span class="sxs-lookup"><span data-stu-id="30d71-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30d71-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-132">12</span><span class="sxs-lookup"><span data-stu-id="30d71-132">12</span></span></p></td>
<td><p><span data-ttu-id="30d71-133">Empêche d'autres utilisateurs d'ouvrir une connexion.</span><span class="sxs-lookup"><span data-stu-id="30d71-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30d71-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-135">0</span><span class="sxs-lookup"><span data-stu-id="30d71-135">0</span></span></p></td>
<td><p><span data-ttu-id="30d71-p103">Par défaut. Indique que les autorisations n'ont pas encore été définies ou qu'elles ne peuvent être déterminées.</span><span class="sxs-lookup"><span data-stu-id="30d71-p103">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30d71-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="30d71-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="30d71-139">2</span><span class="sxs-lookup"><span data-stu-id="30d71-139">2</span></span></p></td>
<td><p><span data-ttu-id="30d71-140">Indique des autorisations en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="30d71-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30d71-141">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="30d71-141">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="30d71-142">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="30d71-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30d71-143">Constante</span><span class="sxs-lookup"><span data-stu-id="30d71-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30d71-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="30d71-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30d71-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="30d71-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30d71-146">(Il n'existe pas d'équivalent pour AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="30d71-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30d71-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="30d71-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30d71-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="30d71-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30d71-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="30d71-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30d71-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="30d71-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30d71-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="30d71-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30d71-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="30d71-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

