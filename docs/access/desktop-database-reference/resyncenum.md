---
title: ResyncEnum (référence de base de données du bureau Access)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3607c0796edb58a6d4227fee09a658220deabfe7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472328"
---
# <a name="resyncenum"></a><span data-ttu-id="ee5f9-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="ee5f9-102">ResyncEnum</span></span>


<span data-ttu-id="ee5f9-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee5f9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ee5f9-104">Spécifie si les valeurs sous-jacentes sont remplacées par un appel à [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ee5f9-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee5f9-105">Constant</span><span class="sxs-lookup"><span data-stu-id="ee5f9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ee5f9-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee5f9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ee5f9-107">Description</span><span class="sxs-lookup"><span data-stu-id="ee5f9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee5f9-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="ee5f9-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="ee5f9-109">2</span><span class="sxs-lookup"><span data-stu-id="ee5f9-109">2</span></span></p></td>
<td><p><span data-ttu-id="ee5f9-p101">Par défaut. Remplace les données, les mises à jour en attente sont annulées.</span><span class="sxs-lookup"><span data-stu-id="ee5f9-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee5f9-112"><strong>adResyncUnderlyingValues</strong></span><span class="sxs-lookup"><span data-stu-id="ee5f9-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="ee5f9-113">1</span><span class="sxs-lookup"><span data-stu-id="ee5f9-113">1</span></span></p></td>
<td><p><span data-ttu-id="ee5f9-114">Ne remplace pas les données, les mises à jour en attente ne sont pas annulées.</span><span class="sxs-lookup"><span data-stu-id="ee5f9-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee5f9-115">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="ee5f9-115">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="ee5f9-116">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ee5f9-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee5f9-117">Constante</span><span class="sxs-lookup"><span data-stu-id="ee5f9-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee5f9-118">AdoEnums.Resync.ALLVALUES</span><span class="sxs-lookup"><span data-stu-id="ee5f9-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee5f9-119">AdoEnums.Resync.UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="ee5f9-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

