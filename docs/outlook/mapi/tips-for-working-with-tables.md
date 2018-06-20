---
title: Conseils pour l’utilisation des tableaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 451bab57d4e2e8669a25d119f9ce28a8f78e628f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787345"
---
# <a name="tips-for-working-with-tables"></a>Conseils pour l’utilisation des tableaux

  
  
**S’applique à**: Outlook 
  
Utilisation d’une MAPI table est un peu comparable à l’utilisation d’une table de base de données relationnelle. Un utilisateur peut limiter le nombre de lignes et colonnes de la vue et spécifier leur ordre. Lignes peuvent être extraites d’un à la fois ou en groupes. Un curseur qui effectue le suivi de la position actuelle peut être déplacé vers un emplacement spécifique dans le tableau. 
  
Pour travailler avec des tableaux, les clients utilisent l’interface en lecture seule, [IMAPITable : IUnknown](imapitableiunknown.md), tandis que les fournisseurs de service, selon qu’ils possèdent les données selon la table, peuvent utiliser soit **IMAPITable** ou [ITableData : IUnknown](itabledataiunknown.md). Les opérations définies dans ces interfaces peuvent être classées en tant qu’opérations que tous les utilisateurs de tableaux ou peuvent appeler et qui ne sont pas aussi largement utilisés, car ils sont plus avancés. Certaines opérations avancées sont plus complexes à implémenter ; d’autres personnes sont ne plus complexes, mais destinées aux petites rarement composants MAPI. 
  
Opérations les plus courantes sont les suivants :
  
- Opérations de colonne, qui affectent les colonnes uniques. Cela inclut la spécification des propriétés à inclure dans l’ensemble de colonnes et l’ordre dans lequel ils doivent être inclus.
    
- Opérations de ligne, qui concerne les lignes uniques. Cela inclut les opérations de maintenance et de récupération des données : ajout, suppression et la modification d’une seule ligne ou plusieurs lignes.
    
- Opérations globales, qui affectent l’intégralité du tableau. Cela inclut la notification d’événement, recherche et le tri.
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

