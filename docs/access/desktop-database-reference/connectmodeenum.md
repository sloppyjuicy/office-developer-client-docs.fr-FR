---
title: ConnectModeEnum (référence de base de données du bureau Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708661"
---
# <a name="connectmodeenum"></a><span data-ttu-id="76d4b-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="76d4b-102">ConnectModeEnum</span></span>

<span data-ttu-id="76d4b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76d4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76d4b-104">Spécifie les autorisations disponibles pour modifier les données dans une [Connexion](connection-object-ado.md), en ouvrant un [Enregistrement](record-object-ado.md), ou en spécifiant des valeurs pour la propriété [Mode](mode-property-ado.md) de l' **Enregistrement** et des objets [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="76d4b-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76d4b-105">Constante</span><span class="sxs-lookup"><span data-stu-id="76d4b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="76d4b-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="76d4b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="76d4b-107">Description</span><span class="sxs-lookup"><span data-stu-id="76d4b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-109">1</span><span class="sxs-lookup"><span data-stu-id="76d4b-109">1</span></span></p></td>
<td><p><span data-ttu-id="76d4b-110">Indique des autorisations en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="76d4b-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76d4b-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-112">3</span><span class="sxs-lookup"><span data-stu-id="76d4b-112">3</span></span></p></td>
<td><p><span data-ttu-id="76d4b-113">Indique des autorisations en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="76d4b-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-114"><strong>encore adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-115">0 x 400000</span><span class="sxs-lookup"><span data-stu-id="76d4b-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="76d4b-116">Utilisée conjointement avec les autres valeurs <em>*ShareDeny*</em> (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>ou <strong>adModeShareDenyRead</strong>) pour propager les restrictions de partage à tous les enregistrements secondaire de l' <strong>enregistrement</strong>actif.</span><span class="sxs-lookup"><span data-stu-id="76d4b-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="76d4b-117">Il n’a aucun effet si l' <strong>enregistrement</strong> n’a pas d’enfants.</span><span class="sxs-lookup"><span data-stu-id="76d4b-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="76d4b-118">Une erreur d’exécution est générée si elle est utilisée avec <strong>adModeShareDenyNone</strong> .</span><span class="sxs-lookup"><span data-stu-id="76d4b-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="76d4b-119">Toutefois, il peut être utilisé avec <strong>adModeShareDenyNone</strong> lorsqu’il est associé avec d’autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="76d4b-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="76d4b-120">Par exemple, vous pouvez utiliser &quot; <strong>adModeRead</strong> ou <strong>adModeShareDenyNone</strong> ou <strong>encore adModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="76d4b-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76d4b-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-122">16</span><span class="sxs-lookup"><span data-stu-id="76d4b-122">16</span></span></p></td>
<td><p><span data-ttu-id="76d4b-p103">Permet à d'autres utilisateurs d'ouvrir une connexion sans autorisations d'aucune sorte. L'accès en lecture et en écriture ne pourra être interdit.</span><span class="sxs-lookup"><span data-stu-id="76d4b-p103">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-126">4</span><span class="sxs-lookup"><span data-stu-id="76d4b-126">4</span></span></p></td>
<td><p><span data-ttu-id="76d4b-127">Empêche d'autres utilisateurs d'ouvrir une connexion sans autorisation de lecture.</span><span class="sxs-lookup"><span data-stu-id="76d4b-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76d4b-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-129">8</span><span class="sxs-lookup"><span data-stu-id="76d4b-129">8</span></span></p></td>
<td><p><span data-ttu-id="76d4b-130">Empêche d'autres utilisateurs d'ouvrir une connexion sans autorisation d'écriture.</span><span class="sxs-lookup"><span data-stu-id="76d4b-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-132">12</span><span class="sxs-lookup"><span data-stu-id="76d4b-132">12</span></span></p></td>
<td><p><span data-ttu-id="76d4b-133">Empêche d'autres utilisateurs d'ouvrir une connexion.</span><span class="sxs-lookup"><span data-stu-id="76d4b-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76d4b-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-135">0</span><span class="sxs-lookup"><span data-stu-id="76d4b-135">0</span></span></p></td>
<td><p><span data-ttu-id="76d4b-p104">Par défaut. Indique que les autorisations n'ont pas encore été définies ou qu'elles ne peuvent être déterminées.</span><span class="sxs-lookup"><span data-stu-id="76d4b-p104">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="76d4b-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="76d4b-139">2</span><span class="sxs-lookup"><span data-stu-id="76d4b-139">2</span></span></p></td>
<td><p><span data-ttu-id="76d4b-140">Indique des autorisations en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="76d4b-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="76d4b-141">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="76d4b-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="76d4b-142">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="76d4b-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76d4b-143">Constante</span><span class="sxs-lookup"><span data-stu-id="76d4b-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="76d4b-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76d4b-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="76d4b-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-146">(Il n'existe pas d'équivalent pour AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="76d4b-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76d4b-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="76d4b-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="76d4b-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76d4b-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="76d4b-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="76d4b-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76d4b-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="76d4b-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76d4b-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="76d4b-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

