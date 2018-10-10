---
title: Caractéristiques de curseur et de verrou
TOCTitle: Cursor and Lock Characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 50eadc486d00436a51b9f7341ef6e0ad2587a015
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469061"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="6d24a-102">Caractéristiques de curseur et de verrou</span><span class="sxs-lookup"><span data-stu-id="6d24a-102">Cursor and Lock Characteristics</span></span>


<span data-ttu-id="6d24a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d24a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6d24a-104">S'il est vrai que les caractéristiques d'un curseur dépendent des fonctionnalités du fournisseur, les avantages et inconvénients suivants s'appliquent généralement aux différents types de curseurs et de verrous.</span><span class="sxs-lookup"><span data-stu-id="6d24a-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d24a-105">Type de curseur ou de verrou</span><span class="sxs-lookup"><span data-stu-id="6d24a-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="6d24a-106">Avantages</span><span class="sxs-lookup"><span data-stu-id="6d24a-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="6d24a-107">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="6d24a-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d24a-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="6d24a-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-109">Ressources requises peu importantes</span><span class="sxs-lookup"><span data-stu-id="6d24a-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-110">Défilement arrière impossible</span><span class="sxs-lookup"><span data-stu-id="6d24a-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="6d24a-111">Pas d'accès concurrentiel aux données</span><span class="sxs-lookup"><span data-stu-id="6d24a-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d24a-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="6d24a-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-113">Défilement possible</span><span class="sxs-lookup"><span data-stu-id="6d24a-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-114">Pas d'accès concurrentiel aux données</span><span class="sxs-lookup"><span data-stu-id="6d24a-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d24a-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="6d24a-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-116">Accès concurrentiel aux données possible mais limité</span><span class="sxs-lookup"><span data-stu-id="6d24a-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="6d24a-117">Défilement possible</span><span class="sxs-lookup"><span data-stu-id="6d24a-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-118">Ressources requises plus importantes</span><span class="sxs-lookup"><span data-stu-id="6d24a-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="6d24a-119">Non disponible dans un scénario déconnecté</span><span class="sxs-lookup"><span data-stu-id="6d24a-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d24a-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="6d24a-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-121">Accès concurrentiel aux données élevé</span><span class="sxs-lookup"><span data-stu-id="6d24a-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="6d24a-122">Défilement possible</span><span class="sxs-lookup"><span data-stu-id="6d24a-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-123">Ressources requises très importantes</span><span class="sxs-lookup"><span data-stu-id="6d24a-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="6d24a-124">Non disponible dans un scénario déconnecté</span><span class="sxs-lookup"><span data-stu-id="6d24a-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d24a-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="6d24a-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-126">Ressources requises peu importantes</span><span class="sxs-lookup"><span data-stu-id="6d24a-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="6d24a-127">Hautement évolutif</span><span class="sxs-lookup"><span data-stu-id="6d24a-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-128">Mise à jour des données par le curseur impossible</span><span class="sxs-lookup"><span data-stu-id="6d24a-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d24a-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="6d24a-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-130">Mises à jour par lot</span><span class="sxs-lookup"><span data-stu-id="6d24a-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="6d24a-131">Scénarios déconnectés autorisés</span><span class="sxs-lookup"><span data-stu-id="6d24a-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="6d24a-132">Accès aux données par d'autres utilisateurs possible</span><span class="sxs-lookup"><span data-stu-id="6d24a-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-133">Données modifiables simultanément par plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6d24a-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d24a-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="6d24a-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-135">Modification des données par d'autres utilisateurs impossible lorsqu'elles sont verrouillées</span><span class="sxs-lookup"><span data-stu-id="6d24a-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-136">Accès aux données par d'autres utilisateurs impossible lorsqu'elles sont verrouillées</span><span class="sxs-lookup"><span data-stu-id="6d24a-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d24a-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="6d24a-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-138">Accès aux données par d'autres utilisateurs possible</span><span class="sxs-lookup"><span data-stu-id="6d24a-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d24a-139">Données modifiables simultanément par plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6d24a-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

