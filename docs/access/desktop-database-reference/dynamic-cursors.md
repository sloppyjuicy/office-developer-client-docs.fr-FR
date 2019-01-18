---
title: Curseurs dynamiques (référence de base de données du bureau Access)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ee81b2bd0e7d40b3a426c6416111d21e2ec760c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726028"
---
# <a name="dynamic-cursors"></a>Curseurs dynamiques


**S’applique à**: Access 2013, Office 2013

Les curseurs dynamiques détectent toutes les modifications apportées aux lignes du jeu de résultats, qu'elles soient effectuées à l'intérieur du curseur ou par d'autres utilisateurs en dehors du curseur. Le curseur vous permet de voir toutes les instructions d'insertion, de mise à jour et de suppression, exécutées par tous les utilisateurs. Une fois le curseur ouvert, le curseur dynamique peut détecter les modifications apportées aux lignes, à l'ordre de tri et aux valeurs du jeu de résultats. Les mises à jour effectuées en dehors du curseur ne sont pas visibles tant qu'elles n'ont pas été validées (à moins que le niveau d'isolation de la transaction du curseur ait une valeur « non validé »).

Supposons, par exemple, qu'un curseur dynamique extrait deux lignes et une autre application avant de mettre à jour une de ces lignes et de supprimer la deuxième. Si le curseur dynamique extrait ces deux lignes, il ne trouvera pas celle qui a été supprimée, en revanche, il affichera les nouvelles valeurs de la ligne mise à jour.

Le choix du curseur dynamique est judicieux si votre application doit détecter toutes les mises à jour apportées simultanément par d'autres utlisateurs. Affectez la valeur **adOpenDynamic** à **CursorTypeEnum** pour indiquer que vous souhaitez utiliser un curseur dynamique dans ADO.

[Curseurs avant uniquement](forward-only-cursors.md) | [Curseurs statiques](static-cursors.md) | [Curseurs avec jeu de clés](keyset-cursors.md)

