---
title: Définition de la position du tableau avec une valeur fractionnaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a569f99065acbb7a099839b078c56c0a0db0658d
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462226"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Définition de la position du tableau avec une valeur fractionnaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les utilisateurs de tableau peuvent se déplacer vers une position qui représente un pourcentage approximatif de lignes par rapport au total. Plutôt que de passer à une ligne exacte, cette méthode de positionnement divise le tableau en parties en fractions. Les utilisateurs de tableau peuvent, par exemple, se déplacer vers le point à mi-chemin d’un tableau ou vers la ligne qui se trouve à 7/8 du chemin du tableau. 
  
 **Pour déplacer le curseur un nombre approximatif de lignes**
  
- [Appelez IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** se déplace vers la ligne qui représente un pourcentage particulier de lignes par rapport au début du tableau. Ce pourcentage est spécifié dans les _paramètres ulNumerator_ et  _ulDenominator_ . **SeekRowApprox est fréquemment utilisé** pour implémenter des barres de défilement. 
    
 **Pour déterminer la position approximative d’un tableau**
  
- [Appelez IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** peut être utilisé pour informer l’utilisateur de la position actuelle. Il définit une valeur fractionnaire en fonction du nombre de lignes du tableau et du numéro de la ligne actuelle. Attendez-vous à ce que cette valeur représente une estimation. Les implémenteurs de tableau sont encouragés à ne pas calculer la position exacte, car les implémentations précises peuvent être coûteuses à appeler, en particulier sur les tableaux catégorisés. 
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

