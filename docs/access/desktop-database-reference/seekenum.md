---
title: SeekEnum (référence de base de données du bureau Access)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5025706d64927482b632a17a5f71839cd4186619
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861413"
---
# <a name="seekenum"></a><span data-ttu-id="8bf36-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="8bf36-102">SeekEnum</span></span>

<span data-ttu-id="8bf36-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bf36-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8bf36-104">Spécifie le type de [Seek](seek-method-ado.md) à exécuter.</span><span class="sxs-lookup"><span data-stu-id="8bf36-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bf36-105">Constant</span><span class="sxs-lookup"><span data-stu-id="8bf36-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8bf36-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bf36-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8bf36-107">Description</span><span class="sxs-lookup"><span data-stu-id="8bf36-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bf36-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="8bf36-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="8bf36-109">1</span><span class="sxs-lookup"><span data-stu-id="8bf36-109">1</span></span></p></td>
<td><p><span data-ttu-id="8bf36-110">Recherche la première clé égale à <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="8bf36-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf36-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="8bf36-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="8bf36-112">2</span><span class="sxs-lookup"><span data-stu-id="8bf36-112">2</span></span></p></td>
<td><p><span data-ttu-id="8bf36-113">Recherche la dernière clé égale à <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="8bf36-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf36-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="8bf36-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="8bf36-115">4</span><span class="sxs-lookup"><span data-stu-id="8bf36-115">4</span></span></p></td>
<td><p><span data-ttu-id="8bf36-116">Recherche soit une clé égale à <em>KeyValues</em>, soit l'emplacement théorique suivant.</span><span class="sxs-lookup"><span data-stu-id="8bf36-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf36-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="8bf36-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="8bf36-118">8</span><span class="sxs-lookup"><span data-stu-id="8bf36-118">8</span></span></p></td>
<td><p><span data-ttu-id="8bf36-119">Recherche une clé à l'emplacement théorique suivant de la correspondance avec <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="8bf36-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf36-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="8bf36-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="8bf36-121">16</span><span class="sxs-lookup"><span data-stu-id="8bf36-121">16</span></span></p></td>
<td><p><span data-ttu-id="8bf36-122">Recherche une clé égale à <em>KeyValues</em>, ou l'emplacement théorique suivant de cette correspondance.</span><span class="sxs-lookup"><span data-stu-id="8bf36-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf36-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="8bf36-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="8bf36-124">32</span><span class="sxs-lookup"><span data-stu-id="8bf36-124">32</span></span></p></td>
<td><p><span data-ttu-id="8bf36-125">Recherche une clé juste avant l'emplacement théorique d'une correspondance avec <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="8bf36-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8bf36-126">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8bf36-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="8bf36-127">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8bf36-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bf36-128">Constante</span><span class="sxs-lookup"><span data-stu-id="8bf36-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bf36-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="8bf36-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf36-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="8bf36-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf36-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="8bf36-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf36-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="8bf36-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf36-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="8bf36-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf36-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="8bf36-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

