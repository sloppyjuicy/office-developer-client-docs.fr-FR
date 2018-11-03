---
title: Curseurs statiques (référence de base de données du bureau Access)
TOCTitle: Static cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac6d55f8869cb273aceb1d55b226ef97585f7f4a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943884"
---
# <a name="static-cursors"></a>Curseurs statiques


**S’applique à**: Access 2013, Office 2013

Le curseur statique affiche toujours le jeu de résultats tel qu'il était à la première ouverture du curseur. Selon l'implémentation, les curseurs statiques peuvent être accessibles en lecture seule ou en lecture/écriture. Ils permettent un défilement avant et arrière. En règle générale, le curseur statique ne détecte pas les modifications d'appartenance, d'ordre ou de valeur du jeu de résultats après l'ouverture du curseur. Les curseurs statiques peuvent détecter leurs propres mises à jour, suppressions et insertions, mais cette fonction n'est pas obligatoire.

Les curseurs statiques ne détectent jamais les autres mises à jour, suppressions et insertions. Supposons par exemple qu'un curseur statique extrait une ligne, laquelle est ensuite mise à jour par une autre application. Si l'application extrait à nouveau la ligne à partir du curseur statique, les valeurs affichées restent inchangées, malgré les modifications apportées par l'application. Tous les types de défilement sont pris en charge, mais tous les fournisseurs ne prennent pas les signets en charge.

Si votre application ne doit pas détecter les modifications de données mais exige des fonctionnalités de défilement, le curseur statique constitue la solution idéale. Utilisez **adOpenStatic** avec **CursorTypeEnum** pour indiquer que vous souhaitez utiliser un curseur statique dans ADO.

