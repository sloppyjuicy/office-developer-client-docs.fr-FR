---
title: Curseurs de type avant uniquement
TOCTitle: Forward-Only Cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 176dc9fe3820b88ddaf0bd27feb4aacbbcb311cc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886283"
---
# <a name="forward-only-cursors"></a>Curseurs de type avant uniquement


**S’applique à**: Access 2013, Office 2013

Le type de curseur par défaut, appellé curseur en avant uniquement (ou non déroulant), ne peut aller que vers l'avant dans le jeu de résultats. Un tel curseur ne prend pas en charge le défilement (la capacité d'avancer et de reculer dans un jeu de résultats) ; il ne prend en charge que l'extraction de lignes du début à la fin du jeu de résultats. Avec certains curseurs de ce type (comme avec la bibliothèque de curseurs SQL Server), toutes les instructions d'insertion, de mise à jour et de suppression réalisées par l'utilisateur actif (ou validées par d'autres utilisateurs) qui affectent les lignes du jeu de résultats sont visibles au moment de leur extraction. Comme le curseur ne peut pas revenir en arrière, les modifications apportées aux lignes de la base de données une fois que ces lignes ont été extraites ne sont pas visibles à travers le curseur.

Une fois les données de la ligne active traitées, le curseur à défilement vers l'avant uniquement libère les ressources utilisées pour conserver ces données. Ces curseurs sont dynamiques par défaut, ce qui signifie que toutes les modifications sont détectées au moment du traitement de la ligne. Ceci permet une ouverture plus rapide du curseur et au jeu de résultats d'afficher les mises à jour réalisées sur les tables sous-jacentes.

Bien que les curseurs à défilement avant uniquement ne prennent pas en charge le défilement arrière, votre application peut revenir au début du jeu de résultats en fermant et rouvrant le curseur. Cette méthode est efficace pour les petites quantités de données. Votre application pourrait également lire le jeu de résultats une première fois, mettre les données en cache localement, puis parcourir les données locales mises en cache.

Si le défilement dans le jeu de résultats n'est pas nécessaire pour votre application, le curseur à défilement avant uniquement constitue le meilleur moyen d'extraire des données rapidement avec une surcharge moindre. Utilisez **adOpenForwardOnly** **CursorTypeEnum** pour indiquer que vous souhaitez utiliser un curseur à défilement avant uniquement dans ADO.

