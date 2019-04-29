---
title: Définition de la position de la table avec une valeur fractionnaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437335"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Définition de la position de la table avec une valeur fractionnaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tableau les utilisateurs peuvent passer à une position qui représente un pourcentage approximatif de lignes par rapport au total. Au lieu de passer à une ligne exacte, cette méthode de positionnement divise le tableau en portions en fonction de fractions. Tableau les utilisateurs peuvent déplacer, par exemple, vers le point de la moitié d'un tableau ou vers la ligne 7/8 du tableau. 
  
 **Pour déplacer le curseur d'un nombre approximatif de lignes**
  
- Appeler [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** passe à la ligne qui représente un pourcentage particulier de lignes par rapport au début de la table. Ce pourcentage est spécifié dans les paramètres _ulNumerator_ et _ulDenominator_ . **SeekRowApprox** est fréquemment utilisé pour implémenter des barres de défilement. 
    
 **Pour déterminer la position approximative d'une table**
  
- Appeler [IMAPITable:: QueryPosition](imapitable-queryposition.md). **QueryPosition** peut être utilisé pour informer l'utilisateur de la position actuelle. Il définit une valeur fractionnaire basée sur le nombre de lignes du tableau et le numéro de la ligne active. Attendez que cette valeur représente une approximation. Les implémenteurs de tableaux sont encouragés à ne pas calculer la position exacte, car les implémentations précises peuvent être coûteuses à appeler, en particulier dans les tables catégorisées. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

