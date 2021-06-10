---
title: Curseurs dynamiques (référence de base de données de bureau Access)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ee81b2bd0e7d40b3a426c6416111d21e2ec760c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293636"
---
# <a name="dynamic-cursors"></a><span data-ttu-id="6c9a5-102">Curseurs dynamiques</span><span class="sxs-lookup"><span data-stu-id="6c9a5-102">Dynamic cursors</span></span>


<span data-ttu-id="6c9a5-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c9a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c9a5-p101">Les curseurs dynamiques détectent toutes les modifications apportées aux lignes du jeu de résultats, qu'elles soient effectuées à l'intérieur du curseur ou par d'autres utilisateurs en dehors du curseur. Le curseur vous permet de voir toutes les instructions d'insertion, de mise à jour et de suppression, exécutées par tous les utilisateurs. Une fois le curseur ouvert, le curseur dynamique peut détecter les modifications apportées aux lignes, à l'ordre de tri et aux valeurs du jeu de résultats. Les mises à jour effectuées en dehors du curseur ne sont pas visibles tant qu'elles n'ont pas été validées (à moins que le niveau d'isolation de la transaction du curseur ait une valeur « non validé »).</span><span class="sxs-lookup"><span data-stu-id="6c9a5-p101">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor. All insert, update, and delete statements made by all users are visible through the cursor. The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened. Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</span></span>

<span data-ttu-id="6c9a5-p102">Supposons, par exemple, qu'un curseur dynamique extrait deux lignes et une autre application avant de mettre à jour une de ces lignes et de supprimer la deuxième. Si le curseur dynamique extrait ces deux lignes, il ne trouvera pas celle qui a été supprimée, en revanche, il affichera les nouvelles valeurs de la ligne mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6c9a5-p102">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other. If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</span></span>

<span data-ttu-id="6c9a5-p103">Le choix du curseur dynamique est judicieux si votre application doit détecter toutes les mises à jour apportées simultanément par d'autres utlisateurs. Affectez la valeur **adOpenDynamic** à **CursorTypeEnum** pour indiquer que vous souhaitez utiliser un curseur dynamique dans ADO.</span><span class="sxs-lookup"><span data-stu-id="6c9a5-p103">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users. Use the **adOpenDynamic** **CursorTypeEnum** to indicate that you want to use a dynamic cursor in ADO.</span></span>

<span data-ttu-id="6c9a5-112">[Curseurs avant uniquement](forward-only-cursors.md) | [Curseurs statiques](static-cursors.md) | [Curseurs avec jeu de clés](keyset-cursors.md)</span><span class="sxs-lookup"><span data-stu-id="6c9a5-112">[Forward-Only Cursors](forward-only-cursors.md) | [Static Cursors](static-cursors.md) | [Keyset Cursors](keyset-cursors.md)</span></span>

