---
title: ConnectModeEnum (référence de base de données de bureau Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295694"
---
# <a name="connectmodeenum"></a><span data-ttu-id="cbaba-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="cbaba-102">ConnectModeEnum</span></span>

<span data-ttu-id="cbaba-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbaba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbaba-104">Spécifie les autorisations disponibles pour modifier les données dans une [Connexion](connection-object-ado.md), en ouvrant un [Enregistrement](record-object-ado.md), ou en spécifiant des valeurs pour la propriété [Mode](mode-property-ado.md) de l’**Enregistrement** et des objets [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cbaba-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbaba-105">Constante</span><span class="sxs-lookup"><span data-stu-id="cbaba-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cbaba-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbaba-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cbaba-107">Description</span><span class="sxs-lookup"><span data-stu-id="cbaba-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-109">0,1</span><span class="sxs-lookup"><span data-stu-id="cbaba-109">1</span></span></p></td>
<td><p><span data-ttu-id="cbaba-110">Indique des autorisations en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cbaba-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbaba-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-112">3</span><span class="sxs-lookup"><span data-stu-id="cbaba-112">3</span></span></p></td>
<td><p><span data-ttu-id="cbaba-113">Indique des autorisations en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="cbaba-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="cbaba-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="cbaba-116">Utilisé conjointement avec les autres valeurs <em>*ShareDeny*</em> (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>ou <strong>adModeShareDenyRead</strong>) pour propager les restrictions de partage à tous les sous-enregistrements de l' <strong>enregistrement</strong>actif.</span><span class="sxs-lookup"><span data-stu-id="cbaba-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="cbaba-117">Elle n'a pas d'effet si l'<strong>Enregistrement</strong> n'a pas d'enfant.</span><span class="sxs-lookup"><span data-stu-id="cbaba-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="cbaba-118">Une erreur d'exécution est générée si elle n'est associée qu'avec <strong>adModeShareDenyNone</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbaba-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="cbaba-119">Elle peut toutefois être s'appliquer à <strong>adModeShareDenyNone</strong> lorsqu'elle est associée à d'autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="cbaba-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="cbaba-120">Par exemple, vous pouvez utiliser &quot; <strong>adModeRead</strong> ou <strong>adModeShareDenyNone</strong> ou <strong>adModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="cbaba-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbaba-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-122">Seiz</span><span class="sxs-lookup"><span data-stu-id="cbaba-122">16</span></span></p></td>
<td><p><span data-ttu-id="cbaba-p103">Permet à d'autres utilisateurs d'ouvrir une connexion sans autorisations d'aucune sorte. L'accès en lecture et en écriture ne pourra être interdit.</span><span class="sxs-lookup"><span data-stu-id="cbaba-p103">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-126">4</span><span class="sxs-lookup"><span data-stu-id="cbaba-126">4</span></span></p></td>
<td><p><span data-ttu-id="cbaba-127">Empêche d'autres utilisateurs d'ouvrir une connexion sans autorisation de lecture.</span><span class="sxs-lookup"><span data-stu-id="cbaba-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbaba-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-129">8bits</span><span class="sxs-lookup"><span data-stu-id="cbaba-129">8</span></span></p></td>
<td><p><span data-ttu-id="cbaba-130">Empêche d'autres utilisateurs d'ouvrir une connexion sans autorisation d'écriture.</span><span class="sxs-lookup"><span data-stu-id="cbaba-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-132">an</span><span class="sxs-lookup"><span data-stu-id="cbaba-132">12</span></span></p></td>
<td><p><span data-ttu-id="cbaba-133">Empêche d'autres utilisateurs d'ouvrir une connexion.</span><span class="sxs-lookup"><span data-stu-id="cbaba-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbaba-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-135">0</span><span class="sxs-lookup"><span data-stu-id="cbaba-135">0</span></span></p></td>
<td><p><span data-ttu-id="cbaba-p104">Par défaut. Indique que les autorisations n'ont pas encore été définies ou qu'elles ne peuvent être déterminées.</span><span class="sxs-lookup"><span data-stu-id="cbaba-p104">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="cbaba-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="cbaba-139">n°2</span><span class="sxs-lookup"><span data-stu-id="cbaba-139">2</span></span></p></td>
<td><p><span data-ttu-id="cbaba-140">Indique des autorisations en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="cbaba-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cbaba-141">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="cbaba-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="cbaba-142">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cbaba-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbaba-143">Constante</span><span class="sxs-lookup"><span data-stu-id="cbaba-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-144">AdoEnums. ConnectMode. READ</span><span class="sxs-lookup"><span data-stu-id="cbaba-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbaba-145">AdoEnums. ConnectMode. READWRITE</span><span class="sxs-lookup"><span data-stu-id="cbaba-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-146">(Il n'existe pas d'équivalent pour AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="cbaba-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbaba-147">AdoEnums. ConnectMode. SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="cbaba-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-148">AdoEnums. ConnectMode. SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="cbaba-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbaba-149">AdoEnums. ConnectMode. SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="cbaba-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-150">AdoEnums. ConnectMode. SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="cbaba-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbaba-151">AdoEnums. ConnectMode. unKNOWn</span><span class="sxs-lookup"><span data-stu-id="cbaba-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbaba-152">AdoEnums. ConnectMode. WRITE</span><span class="sxs-lookup"><span data-stu-id="cbaba-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

