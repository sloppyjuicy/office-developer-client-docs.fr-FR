---
title: Garantie d’espace TempDB suffisant
TOCTitle: Ensuring sufficient TempDB space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e750aebf39a444335194c085900acb8da4380adf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585724"
---
# <a name="ensuring-sufficient-tempdb-space"></a>Garantie d’espace TempDB suffisant


**S’applique à** : Access 2013, Office 2013

Si des erreurs se produisent lors du traitement d'objets [Recordset](recordset-object-ado.md) nécessitant un espace de traitement dans Microsoft SQL Server 6.5, vous serez peut-être amené à augmenter la taille de TempDB. (Certaines requêtes nécessitent un espace de traitement temporaire ; par exemple, une requête assortie d'une clause ORDER BY exige le tri de l'objet **Recordset**, ce qui requiert une certaine quantité d'espace temporaire.)

> [!IMPORTANT]
> [!IMPORTANTE] Lisez cette procédure avant d'effectuer des actions, car il est plus difficile de réduire une unité qui a été préalablement étendue.

> [!NOTE]
> [!REMARQUE] Par défaut, dans Microsoft SQL Server 7.0 et les versions ultérieures, la base de données TempDB est configurée pour croître automatiquement en fonction des besoins. Ainsi, il est possible que cette procédure ne s'applique qu'aux serveurs exécutant des versions antérieures à la version 7.0.



**Pour augmenter l'espace de TempDB dans SQL Server 6.5**

1.  Démarrez Microsoft SQL Server Enterprise Manager, ouvrez l'arborescence Serveur, puis l'arborescence Unités de base de données.

2.  Sélectionnez une unité (physique) à développer, telle que Master, puis double-cliquez sur l'unité pour ouvrir la boîte de dialogue **Edition des unités de base de données**. Cette boîte de dialogue indique la quantité d'espace utilisée par les bases de données actives.

3.  Dans la zone **Taille**, augmentez l'espace disque attribué à l'unité selon la quantité souhaitée (par exemple, 50 mégaoctets (Mo)).

4.  Cliquez sur **Modifier maintenant** pour augmenter la quantité d'espace de la base de données (logique) TempDB.

5.  Ouvrez l'arborescence Bases de données sur le serveur, puis double-cliquez sur **TempDB** pour ouvrir la boîte de dialogue **Edition de la base de données**. L'onglet **Base de données** affiche la quantité d'espace actuellement alloué à TempDB (**Taille des données**). La valeur par défaut est 2 Mo.

6.  Sous le groupe **Taille**, cliquez sur **Développer**. Les graphiques indiquent la quantité d'espace disponible et allouée sur chaque unité physique. Les barres de couleur bordeau représentent l'espace disponible.

7.  Sélectionnez une **unité de journal** (par exemple, Master) pour afficher la taille disponible dans la zone **Taille (Mo)**.

8.  Cliquez sur **Développer maintenant** pour allouer cet espace à la base de données TempDB. La boîte de dialogue **Edition de la base de données** affiche la nouvelle taille allouée à TempDB.

Pour plus d'informations à ce sujet, effectuez une recherche sur « Développement de la base de données, boîte de dialogue » dans le fichier d'aide de Microsoft SQL Server Enterprise Manager.

