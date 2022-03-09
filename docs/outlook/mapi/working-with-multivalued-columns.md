---
title: Travailler avec des colonnes à valeurs multiples
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
ms.openlocfilehash: 1e06054f22b2053aa59249adc78f4e23ef695998
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369258"
---
# <a name="working-with-multivalued-columns"></a>Travailler avec des colonnes à valeurs multiples

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une colonne à valeurs multiples contient les données d’une propriété à valeurs multiples, qui est une propriété qui possède un tableau de valeurs du type de base au lieu d’une valeur unique. Étant donné qu’aucune des tables n’inclut de propriétés à valeurs multiples dans leurs jeux de colonnes par défaut, les propriétés à valeurs multiples ne sont incluses dans une table que si l’utilisateur de la table le demande. 
  
Les colonnes à valeurs multiples peuvent être affichées dans des tableaux :
  
- Sur une seule ligne, toutes les valeurs de propriété apparaissent dans l’instance de colonne unique. Valeur par défaut.
    
    - Ou -
    
- Dans une série de lignes, avec une ligne pour chacune des valeurs de propriété. Chaque valeur unique apparaît dans la colonne dans sa propre ligne avec autant de lignes que de valeurs dans la propriété à valeurs multiples. Chaque ligne a une valeur unique pour la **propriété PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mais les mêmes valeurs pour les autres colonnes. Si une ligne contient plusieurs colonnes avec plusieurs valeurs, par exemple, deux colonnes avec des valeurs _M_ et _N_ respectivement, les instances _MN\*_ de la ligne apparaissent dans le tableau. 
    
Un utilisateur de table demande le type d’affichage non par nature en appelant la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) avec l’indicateur MVI_FLAG définie dans le type de propriété de la colonne à valeurs multiples. L MVI_FLAG est une constante définie en tant que résultat de la combinaison des indicateurs MV_FLAG et MV_INSTANCE avec une opération **LOGIQUE OR** . En plus d’être utilisé dans **SetColumns**, MVI_FLAG peut également être transmis à [IMAPITable::SortTable](imapitable-sorttable.md) dans le paramètre _lpSortCriteria_ et [IMAPITable::Restrict](imapitable-restrict.md) dans le membre **ulPropTag** du paramètre  _lpRestriction_ . Une fois le MVI_FLAG passé, **SortTable** s’exécute de la même manière que **SetColumns**, en ajoutant une ligne pour chaque valeur dans la colonne à valeurs multiples et en triant sur les valeurs individuelles dans les instances. Une ligne est ajoutée pour chaque valeur. 
  
 **Restrict**, cependant, ne développe pas la colonne à valeurs multiples en lignes calculées supplémentaires. Une colonne à valeurs multiples avec le MVI_FLAG indique au fournisseur de services d’utiliser cette colonne pour limiter le tableau. S’il existe une valeur de propriété dans la restriction, il doit s’agit d’une balise de propriété de valeur unique identique à celle qui serait renvoyée par [IMAPITable::QueryRows](imapitable-queryrows.md) pour la colonne. 
  
Les implémenteurs de tableau sont requis uniquement pour prendre en charge le type d’affichage par défaut et peuvent renvoyer la valeur MAPI_E_TOO_COMPLEX lorsqu’un appelant demande l’autre alternative. La possibilité de prendre en charge ces deux types d’affichage est particulièrement importante pour les fournisseurs de magasins de messages qui implémentent des tables de contenu de dossiers. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

