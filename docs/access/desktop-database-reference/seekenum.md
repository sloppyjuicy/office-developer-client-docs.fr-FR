---
title: SeekEnum (référence de base de données de bureau Access)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314657"
---
# <a name="seekenum"></a><span data-ttu-id="93b72-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="93b72-102">SeekEnum</span></span>

<span data-ttu-id="93b72-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="93b72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93b72-104">Spécifie le type de [Seek](seek-method-ado.md) à exécuter.</span><span class="sxs-lookup"><span data-stu-id="93b72-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93b72-105">Constante</span><span class="sxs-lookup"><span data-stu-id="93b72-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="93b72-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="93b72-106">Value</span></span></p></th>
<th><p><span data-ttu-id="93b72-107">Description</span><span class="sxs-lookup"><span data-stu-id="93b72-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93b72-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="93b72-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="93b72-109">1 </span><span class="sxs-lookup"><span data-stu-id="93b72-109">1</span></span></p></td>
<td><p><span data-ttu-id="93b72-110">Recherche la première clé égale à <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="93b72-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93b72-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="93b72-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="93b72-112">2 </span><span class="sxs-lookup"><span data-stu-id="93b72-112">2</span></span></p></td>
<td><p><span data-ttu-id="93b72-113">Recherche la dernière clé égale à <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="93b72-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93b72-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="93b72-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="93b72-115">4 </span><span class="sxs-lookup"><span data-stu-id="93b72-115">4</span></span></p></td>
<td><p><span data-ttu-id="93b72-116">Recherche soit une clé égale à <em>KeyValues</em>, soit l'emplacement théorique suivant.</span><span class="sxs-lookup"><span data-stu-id="93b72-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93b72-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="93b72-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="93b72-118">8 </span><span class="sxs-lookup"><span data-stu-id="93b72-118">8</span></span></p></td>
<td><p><span data-ttu-id="93b72-119">Recherche une clé à l'emplacement théorique suivant de la correspondance avec <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="93b72-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93b72-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="93b72-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="93b72-121">16 </span><span class="sxs-lookup"><span data-stu-id="93b72-121">16</span></span></p></td>
<td><p><span data-ttu-id="93b72-122">Recherche une clé égale à <em>KeyValues</em>, ou l'emplacement théorique suivant de cette correspondance.</span><span class="sxs-lookup"><span data-stu-id="93b72-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93b72-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="93b72-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="93b72-124">32</span><span class="sxs-lookup"><span data-stu-id="93b72-124">32</span></span></p></td>
<td><p><span data-ttu-id="93b72-125">Recherche une clé juste avant l'emplacement théorique d'une correspondance avec <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="93b72-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="93b72-126">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="93b72-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="93b72-127">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="93b72-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93b72-128">Constante</span><span class="sxs-lookup"><span data-stu-id="93b72-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93b72-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="93b72-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93b72-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="93b72-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93b72-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="93b72-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93b72-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="93b72-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93b72-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="93b72-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93b72-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="93b72-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

