---
title: Définition d’une position de table avec une valeur fractionnelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8ffed8070c219e6611aebbcb1dd5cd181b662850
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579696"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Définition d’une position de table avec une valeur fractionnelle

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Les utilisateurs de tableau peuvent déplacer vers une position qui représente un pourcentage approximatif de lignes par rapport au total. Au lieu de passer à une ligne exacte, cette méthode de positionnement divise la table en portions basée sur des fractions. Les utilisateurs de tableau peuvent déplacer, par exemple, à mi-chemin d’une table ou à la ligne qui est 7/8 de la façon dont la table. 
  
 **Pour déplacer le curseur du nombre de lignes approximatif**
  
- Appelez [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** se déplace sur la ligne qui représente un pourcentage de lignes par rapport au début de la table. Ce pourcentage est spécifié dans les paramètres _ulNumerator_ et _ulDenominator_ . **SeekRowApprox** est fréquemment utilisé pour implémenter des barres de défilement. 
    
 **Pour déterminer la position approximative d’une table**
  
- Appelez [IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** peut être utilisé pour informer l’utilisateur de la position actuelle. Il définit une valeur décimale basée sur le nombre de lignes dans le tableau et le nombre de la ligne active. Attendez que cette valeur représente une estimation. L’implémentation de la table est encouragées ne pas à calculer la position exacte étant donné que les implémentations précises coûteuses à appeler, en particulier sur les tableaux, voir. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

