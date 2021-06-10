---
title: Curseurs statiques (référence de base de données de bureau Access)
TOCTitle: Static cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2eb019a6fc960d58771ff5ab0de7dca547c55f1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308539"
---
# <a name="static-cursors"></a><span data-ttu-id="e5f5a-102">Curseurs statiques</span><span class="sxs-lookup"><span data-stu-id="e5f5a-102">Static cursors</span></span>


<span data-ttu-id="e5f5a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5f5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5f5a-p101">Le curseur statique affiche toujours le jeu de résultats tel qu'il était à la première ouverture du curseur. Selon l'implémentation, les curseurs statiques peuvent être accessibles en lecture seule ou en lecture/écriture. Ils permettent un défilement avant et arrière. En règle générale, le curseur statique ne détecte pas les modifications d'appartenance, d'ordre ou de valeur du jeu de résultats après l'ouverture du curseur. Les curseurs statiques peuvent détecter leurs propres mises à jour, suppressions et insertions, mais cette fonction n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e5f5a-p101">The static cursor always displays the result set as it was when the cursor was first opened. Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling. The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened. Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</span></span>

<span data-ttu-id="e5f5a-p102">Les curseurs statiques ne détectent jamais les autres mises à jour, suppressions et insertions. Supposons par exemple qu'un curseur statique extrait une ligne, laquelle est ensuite mise à jour par une autre application. Si l'application extrait à nouveau la ligne à partir du curseur statique, les valeurs affichées restent inchangées, malgré les modifications apportées par l'application. Tous les types de défilement sont pris en charge, mais tous les fournisseurs ne prennent pas les signets en charge.</span><span class="sxs-lookup"><span data-stu-id="e5f5a-p102">Static cursors never detect other updates, deletes, and inserts. For example, suppose a static cursor fetches a row, and another application then updates that row. If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application. All types of scrolling are supported, but providers may or may not support bookmarks.</span></span>

<span data-ttu-id="e5f5a-p103">Si votre application ne doit pas détecter les modifications de données mais exige des fonctionnalités de défilement, le curseur statique constitue la solution idéale. Utilisez **adOpenStatic** avec **CursorTypeEnum** pour indiquer que vous souhaitez utiliser un curseur statique dans ADO.</span><span class="sxs-lookup"><span data-stu-id="e5f5a-p103">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice. Use the **adOpenStatic** **CursorTypeEnum** to indicate that you want to use a static cursor in ADO.</span></span>

