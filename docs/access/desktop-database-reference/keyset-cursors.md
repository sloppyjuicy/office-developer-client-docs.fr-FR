---
title: Curseurs de jeu de clés (référence de base de données de bureau Access)
TOCTitle: Keyset cursors
ms:assetid: 4b6e5f90-4413-4fb3-0a08-2cb89d3c61f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249236(v=office.15)
ms:contentKeyID: 48544690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aba252a92887f5232d4c1af35aaf8345f6ab4d7f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622213"
---
# <a name="keyset-cursors"></a>Curseurs de jeu de clés

**S’applique à** : Access 2013, Office 2013

Sa capacité à détecter les modifications place le curseur de jeu de clés entre le curseur statique et le curseur dynamique. À l'instar du curseur statique, il ne détecte pas toujours les changements apportés à l'appartenance et à l'ordre du jeu de résultats. À l'instar du curseur dynamique, il détecte les changements apportés aux valeurs des lignes du jeu de résultats.

Les curseurs de jeu de clés sont contrôlés par un ensemble d'identificateurs uniques (clés) appelé jeu de clés. Ces clés sont conçues à partir d'un jeu de colonnes qui identifient de manière unique les lignes du jeu de résultats. Le jeu de clés désigne l'ensemble des valeurs de clés de toutes les lignes renvoyées par l'instruction de requête.

Avec les curseurs de jeu de clés, une clé est générée et enregistrée pour chaque ligne du curseur et stockée sur la station de travail cliente ou sur le serveur. Lorsque vous accédez à une ligne, la clé stockée est utilisée pour extraire les valeurs de données courantes de la source de données. Dans un curseur de jeu de clés, l'appartenance du jeu de résultats est figée lorsque le jeu de clés est saturé. Par conséquent, les ajouts ou mises à jour affectant l'appartenance ne font pas partie du jeu de résultats tant qu'il n'est pas rouvert.

Les modifications apportées aux valeurs de données (soit par le propriétaire du jeu de clés, soit par d'autres processus) sont visibles lorsque l'utilisateur fait défiler le jeu de résultats. Les insertions effectuées en dehors du curseur (par d'autres processus) ne sont visibles que si le curseur est fermé, puis rouvert. Les insertions effectuées à l'intérieur du curseur sont visibles à la fin du jeu de résultats.

Lorsqu'un curseur de jeu de clés tente d'extraire une ligne supprimée, la ligne apparaît comme un « trou » dans le jeu de résultats. La clé de la ligne existe dans le jeu de clés, mais la ligne n'existe plus dans le jeu de résultats. Si les valeurs de clés d'une ligne sont mises à jour, la ligne est considérée comme supprimée, puis insérée. Par conséquent, de telles lignes apparaissent comme des trous dans le jeu de résultats. Alors qu'un curseur de jeu de clés peut toujours détecter les lignes supprimées par d'autres processus, il ne peut pas toujours supprimer les clés des lignes qu'il a lui-même supprimées. Les curseurs de jeu de clés qui le font ne peuvent pas détecter leurs propres suppressions car il n'en reste aucune trace.

Une mise à jour d'une colonne de clé se déroule de la façon suivante : l'ancienne clé est d'abord supprimée, puis la nouvelle est insérée. La nouvelle valeur de clé n'est pas visible si la mise à jour n'a pas été réalisée à l'aide du curseur. Si elle a été réalisée avec le curseur, cette valeur apparaît à la fin du jeu de résultats.

Il existe une variante des curseurs de jeu de clés appelée curseurs standard de jeu de clés. Dans ce type de curseur, l'appartenance des lignes du jeu de résultats et leur ordre sont définis à l'ouverture du curseur, mais les modifications apportées aux valeurs par le propriétaire du curseur et les modifications validées réalisées par d'autres processus sont visibles. Si une modification modifie l'appartenance d'une ligne ou affecte son ordre, cette ligne ne disparaît ni ne bouge tant que le curseur n'est pas fermé, puis rouvert. Les données insérées n'apparaissent pas, mais les changements apportés aux données existantes apparaissent lorsque les lignes sont extraites.

Le curseur de jeu de clés est difficile à utiliser correctement car la sensibilité envers les changements de données dépend d'une variété de circonstances différentes, comme décrit ci-dessus. Cependant, si votre application n'est pas affectée par les mises à jour concurrentes, peut gérer les mauvaises clés avec des programmes et doit accéder directement à certaines lignes dotées de clés, ce type de curseur vous convient. Utilisez **adOpenKeyset** **CursorTypeEnum** pour signaler que vous souhaitez utiliser un curseur de jeu de clés dans ADO.

