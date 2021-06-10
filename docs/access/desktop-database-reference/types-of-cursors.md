---
title: Types de curseurs (référence de base de données de bureau Access)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6493d746f43ac8d923e5b1b9d6dcd3de44b411ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314027"
---
# <a name="types-of-cursors"></a><span data-ttu-id="96f34-102">Types de curseurs</span><span class="sxs-lookup"><span data-stu-id="96f34-102">Types of cursors</span></span>


<span data-ttu-id="96f34-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96f34-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96f34-p101">En règle générale, votre application doit utiliser le curseur le plus simple possible, capable de fournir l'accès aux données requis. Toutes les caractéristiques supplémentaires au-delà des fonctions de base (avant uniquement, lecture seule, statique, défilement, sans tampon) sont susceptibles d'avoir une incidence sur la mémoire du client, la charge réseau ou les performances. Dans la plupart des cas, les options du curseur par défaut génèrent un curseur plus complexe que celui nécessaire à votre application.</span><span class="sxs-lookup"><span data-stu-id="96f34-p101">As a general rule, your application should use the simplest cursor that provides the required data access. Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance. In many cases, the default cursor options generate a more complex cursor than your application actually needs.</span></span>

<span data-ttu-id="96f34-107">Le choix du type de curseur dépend de plusieurs éléments : la façon dont votre application utilise le jeu de résultats et diverses considérations de conception, notamment la taille du jeu de résultats, le pourcentage de données susceptibles d'être utilisées, le degré de sensibilité aux modifications de données et les performances d'application requises.</span><span class="sxs-lookup"><span data-stu-id="96f34-107">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</span></span>

<span data-ttu-id="96f34-108">Au niveau le plus élémentaire, le choix de curseur varie selon que vous devez modifier les données ou simplement les consulter :</span><span class="sxs-lookup"><span data-stu-id="96f34-108">At its most basic, your cursor choice depends on whether you need to change or simply view the data:</span></span>

  - <span data-ttu-id="96f34-109">Si vous devez parcourir un jeu de résultats sans modifier de données, utilisez un curseur [avant uniquement](forward-only-cursors.md) ou un curseur [statique](static-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="96f34-109">If you just need to scroll through a set of results, but not change data, use a [forward-only](forward-only-cursors.md) or [static](static-cursors.md) cursor.</span></span>

  - <span data-ttu-id="96f34-110">Si votre jeu de résultats est volumineux et que vous devez sélectionner uniquement quelques lignes, utilisez un curseur de type [jeu de clés](keyset-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="96f34-110">If you have a large result set and need to select just a few rows, use a [keyset](keyset-cursors.md) cursor.</span></span>

  - <span data-ttu-id="96f34-111">Si vous souhaitez synchroniser un jeu de résultats avec les ajouts, les modifications et les suppressions récents effectués simultanément par tous les utilisateurs, utilisez un curseur [dynamique](dynamic-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="96f34-111">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a [dynamic](dynamic-cursors.md) cursor.</span></span>

<span data-ttu-id="96f34-112">Bien que chaque curseur semble différent, rappelez-vous que ces types de curseur ne présentent pas de différences majeures et possèdent souvent des caractéristiques et des options communes.</span><span class="sxs-lookup"><span data-stu-id="96f34-112">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</span></span>

