---
title: Position de la Table paramètre avec une valeur décimale
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 104de38a41408091a6fbb69995de4f41f6fea6a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787140"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Position de la Table paramètre avec une valeur décimale

  
  
**S’applique à**: Outlook 
  
Les utilisateurs de tableau peuvent déplacer vers une position qui représente un pourcentage approximatif de lignes par rapport au total. Au lieu de passer à une ligne exacte, cette méthode de positionnement divise la table en portions basée sur des fractions. Les utilisateurs de tableau peuvent déplacer, par exemple, à mi-chemin d’une table ou à la ligne qui est 7/8 de la façon dont la table. 
  
 **Pour déplacer le curseur du nombre de lignes approximatif**
  
- Appelez [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** se déplace sur la ligne qui représente un pourcentage de lignes par rapport au début de la table. Ce pourcentage est spécifié dans les paramètres _ulNumerator_ et _ulDenominator_ . **SeekRowApprox** est fréquemment utilisé pour implémenter des barres de défilement. 
    
 **Pour déterminer la position approximative d’une table**
  
- Appelez [IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** peut être utilisé pour informer l’utilisateur de la position actuelle. Il définit une valeur décimale basée sur le nombre de lignes dans le tableau et le nombre de la ligne active. Attendez que cette valeur représente une estimation. L’implémentation de la table est encouragées ne pas à calculer la position exacte étant donné que les implémentations précises coûteuses à appeler, en particulier sur les tableaux, voir. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

