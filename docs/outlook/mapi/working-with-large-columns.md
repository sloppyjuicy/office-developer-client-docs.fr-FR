---
title: Travailler avec des colonnes de grande taille
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
ms.openlocfilehash: f14a3b78ac21b9765ca600ab59412d9faeb59aa4
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378981"
---
# <a name="working-with-large-columns"></a>Travailler avec des colonnes de grande taille

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les colonnes avec des données de chaîne ou de propriété binaire peuvent être de grande taille, voire plusieurs milliers d’octets. Étant donné que l’utilisation d’une ou de plusieurs colonnes avec des centaines d’octets dans un affichage est souvent peu pratique, MAPI permet aux implémenteurs de table de tronque la valeur, le plus souvent à 255 octets et moins souvent à 510 octets. Dans la mesure du possible, les implémenteurs de table doivent inclure la valeur complète d’une propriété dans une colonne de tableau. L’alternative recommandée consiste à inclure uniquement les 255 premiers octets.
  
Les clients ne peuvent pas savoir à l’avance si une table qu’ils utilisent tronque de grandes colonnes. Ils doivent supposer qu’une colonne représente une propriété tronquée si la longueur de la colonne est de 255 ou 510 octets. Si nécessaire, les clients peuvent récupérer directement la valeur complète d’une colonne tronquée de l’objet en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’objet. 
  
Les clients qui imposent des restrictions de construction avec des propriétés de grande taille doivent savoir que c’est à l’implémenteur de la table de se rendre compte du fonctionnement de ces restrictions. Certains implémenteurs de tableau permettent aux restrictions qui sont construites avec une colonne tronquée d’être basées sur la taille tronquée, tandis que d’autres la basent sur la valeur entière. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

