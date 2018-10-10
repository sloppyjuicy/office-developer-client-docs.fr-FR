---
title: Curseurs statiques (référence de base de données du bureau Access)
TOCTitle: Static Cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8878333c8390ffcc075c0160f246e7f16757d226
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471393"
---
# <a name="static-cursors"></a><span data-ttu-id="3cdc9-102">Curseurs statiques</span><span class="sxs-lookup"><span data-stu-id="3cdc9-102">Static Cursors</span></span>


<span data-ttu-id="3cdc9-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cdc9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3cdc9-p101">Le curseur statique affiche toujours le jeu de résultats tel qu'il était à la première ouverture du curseur. Selon l'implémentation, les curseurs statiques peuvent être accessibles en lecture seule ou en lecture/écriture. Ils permettent un défilement avant et arrière. En règle générale, le curseur statique ne détecte pas les modifications d'appartenance, d'ordre ou de valeur du jeu de résultats après l'ouverture du curseur. Les curseurs statiques peuvent détecter leurs propres mises à jour, suppressions et insertions, mais cette fonction n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3cdc9-p101">The static cursor always displays the result set as it was when the cursor was first opened. Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling. The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened. Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</span></span>

<span data-ttu-id="3cdc9-p102">Les curseurs statiques ne détectent jamais les autres mises à jour, suppressions et insertions. Supposons par exemple qu'un curseur statique extrait une ligne, laquelle est ensuite mise à jour par une autre application. Si l'application extrait à nouveau la ligne à partir du curseur statique, les valeurs affichées restent inchangées, malgré les modifications apportées par l'application. Tous les types de défilement sont pris en charge, mais tous les fournisseurs ne prennent pas les signets en charge.</span><span class="sxs-lookup"><span data-stu-id="3cdc9-p102">Static cursors never detect other updates, deletes, and inserts. For example, suppose a static cursor fetches a row, and another application then updates that row. If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application. All types of scrolling are supported, but providers may or may not support bookmarks.</span></span>

<span data-ttu-id="3cdc9-p103">Si votre application ne doit pas détecter les modifications de données mais exige des fonctionnalités de défilement, le curseur statique constitue la solution idéale. Utilisez **adOpenStatic** avec **CursorTypeEnum** pour indiquer que vous souhaitez utiliser un curseur statique dans ADO.</span><span class="sxs-lookup"><span data-stu-id="3cdc9-p103">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice. Use the **adOpenStatic** **CursorTypeEnum** to indicate that you want to use a static cursor in ADO.</span></span>

