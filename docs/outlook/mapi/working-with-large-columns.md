---
title: Utilisation des colonnes de grande taille
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a191a8551d425d7e8b3b9a281936a4a0e2dfd587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787466"
---
# <a name="working-with-large-columns"></a>Utilisation des colonnes de grande taille

  
  
**S’applique à**: Outlook 
  
Colonnes avec des données de propriété binaire ou chaîne pouvant être volumineux, voire des milliers d’octets. Y compris une ou plusieurs colonnes avec des centaines d’octets dans un affichage est souvent difficile, MAPI permet l’implémentation de la table à tronquer la valeur, la plupart du temps à 255 octets et moins souvent 510 octets. La mesure du possible, l’implémentation de la table doit inclure la valeur complète d’une propriété dans une colonne de table. L’alternative recommandée consiste à inclure uniquement les 255 premiers octets.
  
Les clients ne peut pas savoir à l’avance si une table qu’ils utilisent tronque colonnes de grande taille. Ils doivent supposer qu’une colonne représente une propriété tronquée si la longueur de la colonne est 255 ou 510 octets. Si nécessaire, les clients peuvent directement récupérer la valeur d’une colonne tronquée complète de l’objet en appelant la méthode l’objet [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
Création des restrictions de grandes propriétés des clients doivent être conscients qu’il est à l’implémentation de la table quant à ces restrictions de fonctionner. Certains programmeurs table autoriser les restrictions qui sont créées avec une colonne tronquée selon la taille tronquée tandis que d’autres personnes selon la valeur entière. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

