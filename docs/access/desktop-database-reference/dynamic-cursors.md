---
title: Curseurs dynamiques (référence de base de données de bureau Access)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 874f63e765e50ee127c9f2e0009dd164f247450d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602765"
---
# <a name="dynamic-cursors"></a>Curseurs dynamiques


**S’applique à** : Access 2013, Office 2013

Les curseurs dynamiques détectent toutes les modifications apportées aux lignes du jeu de résultats, qu'elles soient effectuées à l'intérieur du curseur ou par d'autres utilisateurs en dehors du curseur. Le curseur vous permet de voir toutes les instructions d'insertion, de mise à jour et de suppression, exécutées par tous les utilisateurs. Une fois le curseur ouvert, le curseur dynamique peut détecter les modifications apportées aux lignes, à l'ordre de tri et aux valeurs du jeu de résultats. Les mises à jour effectuées en dehors du curseur ne sont pas visibles tant qu'elles n'ont pas été validées (à moins que le niveau d'isolation de la transaction du curseur ait une valeur « non validé »).

Supposons, par exemple, qu'un curseur dynamique extrait deux lignes et une autre application avant de mettre à jour une de ces lignes et de supprimer la deuxième. Si le curseur dynamique extrait ces deux lignes, il ne trouvera pas celle qui a été supprimée, en revanche, il affichera les nouvelles valeurs de la ligne mise à jour.

Le choix du curseur dynamique est judicieux si votre application doit détecter toutes les mises à jour apportées simultanément par d'autres utlisateurs. Affectez la valeur **adOpenDynamic** à **CursorTypeEnum** pour indiquer que vous souhaitez utiliser un curseur dynamique dans ADO.

[Curseurs avant uniquement](forward-only-cursors.md) | [Curseurs statiques](static-cursors.md) | [Curseurs avec jeu de clés](keyset-cursors.md)

