---
title: Curseurs de transfert uniquement
TOCTitle: Forward-only cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65eaafe805eabbac1681aa6dcd08b6b99bb056fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292292"
---
# <a name="forward-only-cursors"></a><span data-ttu-id="65ce2-102">Curseurs de transfert uniquement</span><span class="sxs-lookup"><span data-stu-id="65ce2-102">Forward-only cursors</span></span>

<span data-ttu-id="65ce2-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65ce2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65ce2-p101">Le type de curseur par défaut, appellé curseur en avant uniquement (ou non déroulant), ne peut aller que vers l'avant dans le jeu de résultats. Un tel curseur ne prend pas en charge le défilement (la capacité d'avancer et de reculer dans un jeu de résultats) ; il ne prend en charge que l'extraction de lignes du début à la fin du jeu de résultats. Avec certains curseurs de ce type (comme avec la bibliothèque de curseurs SQL Server), toutes les instructions d'insertion, de mise à jour et de suppression réalisées par l'utilisateur actif (ou validées par d'autres utilisateurs) qui affectent les lignes du jeu de résultats sont visibles au moment de leur extraction. Comme le curseur ne peut pas revenir en arrière, les modifications apportées aux lignes de la base de données une fois que ces lignes ont été extraites ne sont pas visibles à travers le curseur.</span><span class="sxs-lookup"><span data-stu-id="65ce2-p101">The typical default cursor type, called a forward-only (or non-scrollable) cursor, can move only forward through the result set. A forward-only cursor does not support scrolling (the ability to move forward and backward in the result set); it only supports fetching rows from the start to the end of the result set. With some forward-only cursors (such as with the SQL Server cursor library), all insert, update, and delete statements made by the current user (or committed by other users) that affect rows in the result set are visible as the rows are fetched. Because the cursor cannot be scrolled backward, however, changes made to rows in the database after the row was fetched are not visible through the cursor.</span></span>

<span data-ttu-id="65ce2-p102">Une fois les données de la ligne active traitées, le curseur à défilement vers l'avant uniquement libère les ressources utilisées pour conserver ces données. Ces curseurs sont dynamiques par défaut, ce qui signifie que toutes les modifications sont détectées au moment du traitement de la ligne. Ceci permet une ouverture plus rapide du curseur et au jeu de résultats d'afficher les mises à jour réalisées sur les tables sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="65ce2-p102">After the data for the current row is processed, the forward-only cursor releases the resources that were used to hold that data. Forward-only cursors are dynamic by default, meaning that all changes are detected as the current row is processed. This provides faster cursor opening and enables the result set to display updates made to the underlying tables.</span></span>

<span data-ttu-id="65ce2-p103">Bien que les curseurs à défilement avant uniquement ne prennent pas en charge le défilement arrière, votre application peut revenir au début du jeu de résultats en fermant et rouvrant le curseur. Cette méthode est efficace pour les petites quantités de données. Votre application pourrait également lire le jeu de résultats une première fois, mettre les données en cache localement, puis parcourir les données locales mises en cache.</span><span class="sxs-lookup"><span data-stu-id="65ce2-p103">While forward-only cursors do not support backward scrolling, your application can return to the beginning of the result set by closing and reopening the cursor. This is an effective way to work with small amounts of data. As an alternative, your application could read the result set once, cache the data locally, and then browse the local data cache.</span></span>

<span data-ttu-id="65ce2-p104">Si le défilement dans le jeu de résultats n'est pas nécessaire pour votre application, le curseur à défilement avant uniquement constitue le meilleur moyen d'extraire des données rapidement avec une surcharge moindre. Utilisez **adOpenForwardOnly** **CursorTypeEnum** pour indiquer que vous souhaitez utiliser un curseur à défilement avant uniquement dans ADO.</span><span class="sxs-lookup"><span data-stu-id="65ce2-p104">If your application does not require scrolling through the result set, the forward-only cursor is the best way to retrieve data quickly with the least amount of overhead. Use the **adOpenForwardOnly** **CursorTypeEnum** to indicate that you want to use a forward-only cursor in ADO.</span></span>

