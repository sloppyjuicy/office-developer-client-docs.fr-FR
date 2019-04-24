---
title: Conseils pour utiliser des tableaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339647"
---
# <a name="tips-for-working-with-tables"></a>Conseils pour utiliser des tableaux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Travailler avec une table MAPI est un peu semblable à travailler avec une table de base de données relationnelle. Un utilisateur peut limiter le nombre de lignes et de colonnes dans l'affichage et spécifier son ordre. Les lignes peuvent être récupérées une par une ou dans des groupes. Un curseur qui effectue le suivi de la position actuelle peut être déplacé vers un emplacement spécifique dans le tableau. 
  
Pour travailler avec des tables, les clients utilisent l'interface en lecture seule, [IMAPITable: IUnknown](imapitableiunknown.md), tandis que les fournisseurs de services, selon qu'ils possèdent ou non les données sur lesquelles la table est basée, peuvent utiliser la fonction **IMAPITable** ou [ITableData: IUnknown](itabledataiunknown.md). Les opérations définies dans ces interfaces peuvent être catégorisées comme des opérations que tous les utilisateurs de tables effectuent ou peuvent appeler et des opérations qui ne sont pas aussi largement utilisées car elles sont plus avancées. Certaines des opérations avancées sont plus complexes à mettre en œuvre; d'autres ne sont pas plus complexes, mais présentent un intérêt pour une petite minorité de composants MAPI. 
  
Les opérations les plus courantes sont les suivantes:
  
- Les opérations sur les colonnes, qui affectent des colonnes uniques. Il s'agit notamment de spécifier les propriétés à inclure dans le jeu de colonnes et l'ordre dans lequel elles doivent être incluses.
    
- Les opérations de ligne, qui affectent des lignes uniques. Il s'agit notamment des opérations de récupération des données et de maintenance: ajout, suppression et modification d'une ou de plusieurs lignes.
    
- Les opérations globales, qui affectent l'intégralité du tableau. Cela inclut la notification d'événement, la recherche et le tri.
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

