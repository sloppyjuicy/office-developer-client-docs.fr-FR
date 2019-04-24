---
title: Utilisation de colonnes de grande taille
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325780"
---
# <a name="working-with-large-columns"></a>Utilisation de colonnes de grande taille

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les colonnes avec des données de propriété binaire ou de chaîne peuvent être volumineuses, voire plusieurs milliers d'octets. Étant donné que l'inclusion d'une ou plusieurs colonnes avec des centaines d'octets dans une vue est souvent peu pratique, MAPI permet aux implémenteurs de tableau de tronquer la valeur, le plus souvent à 255 octets et moins souvent à 510 octets. Dans la mesure du possible, les implémenteurs de tableaux doivent inclure la valeur complète d'une propriété dans une colonne de tableau. L'alternative recommandée consiste à inclure uniquement les premiers 255 octets.
  
Les clients ne peuvent pas savoir à l'avance si une table qu'ils utilisent tronque des colonnes de grande taille. Elles doivent supposer qu'une colonne représente une propriété tronquée si la longueur de la colonne est de 255 ou 510 octets. Si nécessaire, les clients peuvent récupérer directement la valeur complète d'une colonne tronquée à partir de l'objet en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'objet. 
  
Les clients qui créent des restrictions avec des propriétés importantes doivent être conscients du fait que la mise en œuvre de la table est la manière dont ces restrictions fonctionnent. Certains implémenteurs de tableau permettent à des restrictions créées à l'aide d'une colonne tronquée de se fonder sur la taille tronquée, tandis que d'autres le basent sur la valeur entière. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

