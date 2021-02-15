---
title: Caractéristiques du curseur et du verrou
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41a42aa3b0c49a5d871fa7b079a26c7d8076116a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295288"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="7aa4d-102">Caractéristiques du curseur et du verrou</span><span class="sxs-lookup"><span data-stu-id="7aa4d-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="7aa4d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7aa4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7aa4d-104">S'il est vrai que les caractéristiques d'un curseur dépendent des fonctionnalités du fournisseur, les avantages et inconvénients suivants s'appliquent généralement aux différents types de curseurs et de verrous.</span><span class="sxs-lookup"><span data-stu-id="7aa4d-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7aa4d-105">Type de curseur ou de verrou</span><span class="sxs-lookup"><span data-stu-id="7aa4d-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="7aa4d-106">Avantages</span><span class="sxs-lookup"><span data-stu-id="7aa4d-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="7aa4d-107">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="7aa4d-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aa4d-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="7aa4d-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-109">Ressources requises peu importantes</span><span class="sxs-lookup"><span data-stu-id="7aa4d-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-110">Défilement arrière impossible</span><span class="sxs-lookup"><span data-stu-id="7aa4d-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="7aa4d-111">Pas d'accès concurrentiel aux données</span><span class="sxs-lookup"><span data-stu-id="7aa4d-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa4d-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="7aa4d-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-113">Scrollable</span><span class="sxs-lookup"><span data-stu-id="7aa4d-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-114">Pas d'accès concurrentiel aux données</span><span class="sxs-lookup"><span data-stu-id="7aa4d-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa4d-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="7aa4d-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-116">Accès concurrentiel aux données possible mais limité</span><span class="sxs-lookup"><span data-stu-id="7aa4d-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="7aa4d-117">Scrollable</span><span class="sxs-lookup"><span data-stu-id="7aa4d-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-118">Ressources requises plus importantes</span><span class="sxs-lookup"><span data-stu-id="7aa4d-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="7aa4d-119">Non disponible dans un scénario déconnecté</span><span class="sxs-lookup"><span data-stu-id="7aa4d-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa4d-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="7aa4d-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-121">Accès concurrentiel aux données élevé</span><span class="sxs-lookup"><span data-stu-id="7aa4d-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="7aa4d-122">Scrollable</span><span class="sxs-lookup"><span data-stu-id="7aa4d-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-123">Ressources requises très importantes</span><span class="sxs-lookup"><span data-stu-id="7aa4d-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="7aa4d-124">Non disponible dans un scénario déconnecté</span><span class="sxs-lookup"><span data-stu-id="7aa4d-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa4d-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="7aa4d-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-126">Ressources requises peu importantes</span><span class="sxs-lookup"><span data-stu-id="7aa4d-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="7aa4d-127">Hautement évolutif</span><span class="sxs-lookup"><span data-stu-id="7aa4d-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-128">Mise à jour des données par le curseur impossible</span><span class="sxs-lookup"><span data-stu-id="7aa4d-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa4d-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="7aa4d-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-130">Mises à jour par lot</span><span class="sxs-lookup"><span data-stu-id="7aa4d-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="7aa4d-131">Scénarios déconnectés autorisés</span><span class="sxs-lookup"><span data-stu-id="7aa4d-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="7aa4d-132">Accès aux données par d'autres utilisateurs possible</span><span class="sxs-lookup"><span data-stu-id="7aa4d-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-133">Données modifiables simultanément par plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7aa4d-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa4d-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="7aa4d-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-135">Modification des données par d'autres utilisateurs impossible lorsqu'elles sont verrouillées</span><span class="sxs-lookup"><span data-stu-id="7aa4d-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-136">Accès aux données par d'autres utilisateurs impossible lorsqu'elles sont verrouillées</span><span class="sxs-lookup"><span data-stu-id="7aa4d-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa4d-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="7aa4d-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-138">Accès aux données par d'autres utilisateurs possible</span><span class="sxs-lookup"><span data-stu-id="7aa4d-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="7aa4d-139">Données modifiables simultanément par plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7aa4d-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

