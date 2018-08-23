---
title: Utilisation de colonnes à valeurs multiples
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 78f6083cf17bb21152df1a7ea09825f3be7f0e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572941"
---
# <a name="working-with-multivalued-columns"></a>Utilisation de colonnes à valeurs multiples

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une colonne à plusieurs valeurs contienne les données d’une propriété à valeurs multiples, qui est une propriété qui a un tableau de valeurs du type de base au lieu d’une valeur unique. Car aucune table inclure des propriétés à valeurs multiples dans leurs jeux de colonnes par défaut, les propriétés à valeurs multiples sont incluses dans une table uniquement si la demande de l’utilisateur de la table. 
  
Colonnes à valeurs multiples peuvent être affichées dans les tableaux :
  
- Une seule ligne, avec toutes les valeurs de propriété qui apparaissent dans l’instance de colonne unique. Il s’agit de la valeur par défaut.
    
    - Ou -
    
- Dans une série de lignes, avec une ligne pour chacune des valeurs de propriété. Chaque valeur unique s’affiche dans la colonne dans sa propre ligne avec là étant comme le nombre de lignes comme y est des valeurs dans la propriété à valeurs multiples. Chaque ligne contient une valeur unique pour la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mais les mêmes valeurs pour les autres colonnes. Si une ligne contient plusieurs colonnes avec plusieurs valeurs, par exemple, deux colonnes avec _M_ et _N_ valeurs respectivement, puis _M\*N_ les instances de la ligne s’affichent dans le tableau. 
    
Un utilisateur de la table demande le type par défaut d’affichage en appelant la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) avec l’indicateur MVI_FLAG défini dans le type de propriété de la colonne à valeurs multiples. L’indicateur MVI_FLAG est une constante définie comme le résultat de la combinaison d’indicateurs MV_FLAG et MV_INSTANCE avec une opération **OR** logique. Outre utilisé dans **SetColumns**, MVI_FLAG peut également être passé à [IMAPITable::SortTable](imapitable-sorttable.md) dans le paramètre _lpSortCriteria_ et [IMAPITable](imapitable-restrict.md) dans le membre **ulPropTag** de la _lpRestriction_ paramètre. Lorsqu’il est passé à la MVI_FLAG, **SortTable** fonctionne de façon similaire à **SetColumns**, ajout d’une ligne pour chaque valeur dans la colonne à valeurs multiples et de tri des valeurs uniques dans les cas. Une ligne est ajoutée pour chaque valeur. 
  
 **Restrict**, mais n’étend pas la colonne à valeurs multiples en lignes calculées supplémentaires. Une colonne à valeurs multiples avec le jeu de MVI_FLAG indique le fournisseur de services à utiliser cette colonne dans une restriction sur le tableau. Si la restriction est une valeur de propriété, il doit être une balise de propriété seule valeur identique à celle qui est renvoyé par [IMAPITable::QueryRows](imapitable-queryrows.md) pour la colonne. 
  
L’implémentation de la table est uniquement requis pour prendre en charge le type d’affichage par défaut et peut renvoyer la valeur MAPI_E_TOO_COMPLEX lorsqu’un appelant demande l’autre moyen. La possibilité de prendre en charge les deux types d’affichage est plus importante pour les fournisseurs de banque de message l’implémentation de tables de contenu de dossier. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

