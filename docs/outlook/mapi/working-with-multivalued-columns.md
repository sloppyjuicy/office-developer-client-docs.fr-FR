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
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420184"
---
# <a name="working-with-multivalued-columns"></a>Utilisation de colonnes à valeurs multiples

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une colonne à valeurs multiples contient les données d'une propriété à valeurs multiples, qui est une propriété qui a un tableau de valeurs du type de base au lieu d'une valeur unique. Comme aucune des tables n'inclut de propriétés à valeurs multiples dans leurs jeux de colonnes par défaut, les propriétés à valeurs multiples ne sont incluses dans un tableau que si l'utilisateur de la table le demande. 
  
Les colonnes à valeurs multiples peuvent être affichées dans des tableaux:
  
- Sur une seule ligne, avec toutes les valeurs de propriété qui apparaissent dans l'instance de colonne unique. Il s'agit du paramétrage par défaut.
    
    - Des
    
- Dans une série de lignes, avec une ligne pour chacune des valeurs de propriété. Chaque valeur unique apparaît dans la colonne de sa propre ligne avec autant de lignes qu'il y a de valeurs dans la propriété à valeurs multiples. Chaque ligne a une valeur unique pour la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mais les mêmes valeurs pour les autres colonnes. Si une ligne contient plusieurs colonnes avec plusieurs valeurs, par exemple, deux colonnes avec des valeurs _m_ et _N_ respectivement, alors _m\*N_ instances de la ligne apparaissent dans le tableau. 
    
Un utilisateur de tableau demande le type d'affichage non défini par défaut en appelant la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) avec l'indicateur MVI_FLAG défini dans le type de propriété de la colonne à valeurs multiples. L'indicateur MVI_FLAG est une constante définie en tant que résultat de la combinaison des indicateurs MV_FLAG et MV_INSTANCE avec une opération **or** logique. En plus d'être utilisé en **SetColumns**, MVI_FLAG peut également être transmis à une opération [IMAPITable:: SortTable](imapitable-sorttable.md) dans le paramètre _lpSortCriteria_ et [IMAPITable:: Restrict](imapitable-restrict.md) dans le membre **ulPropTag** du _lpRestriction_ paramétré. Une fois le MVI_FLAG passé, **SortTable** s'exécute de la même manière que la fonction **SetColumns**, en ajoutant une ligne pour chaque valeur dans la colonne à valeurs multiples et en triant les valeurs uniques dans les instances. Une ligne est ajoutée pour chaque valeur. 
  
 **** Toutefois, la propriété Restrict ne développe pas la colonne à valeurs multiples en lignes calculées supplémentaires. Une colonne à valeurs multiples avec le jeu MVI_FLAG indique au fournisseur de services d'utiliser cette colonne dans le tableau. S'il y a une valeur de propriété dans la restriction, il doit s'agir d'une balise de propriété à valeur unique identique à celle renvoyée par l'opération [IMAPITable:: QueryRows](imapitable-queryrows.md) pour la colonne. 
  
Les implémenteurs de tableau sont uniquement requis pour prendre en charge le type d'affichage par défaut et peuvent renvoyer la valeur MAPI_E_TOO_COMPLEX lorsqu'un appelant demande l'autre alternative. La possibilité de prendre en charge les deux types d'affichage est essentielle pour les fournisseurs de banque de messages implémentant des tables de contenu de dossier. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

