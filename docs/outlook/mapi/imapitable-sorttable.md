---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432365"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La méthode **IMAPITable:: SortTable** trie les lignes de la table, en fonction des critères de tri. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_lpSortCriteria_
  
> dans Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui contient les critères de tri à appliquer. Le passage d'une structure **SSortOrderSet** qui contient zéro colonne indique que la table n'a pas à être triée dans un ordre particulier. 
    
_ulFlags_
  
> dans Masque de des indicateurs qui contrôle le moment de l'opération **IMAPITable:: SortTable** . Les indicateurs suivants peuvent être définis: 
    
TBL_ASYNC 
  
> Démarre l'opération de manière asynchrone et revient avant la fin de l'opération.
    
TBL_BATCH 
  
> Diffère la fin du tri jusqu'à ce que les données de la table soient requises.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération de tri a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de tri. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne prend pas en charge le type de tri demandé.
    
MAPI_E_TOO_COMPLEX 
  
> Le tableau ne peut pas effectuer l'opération, car les critères de tri particuliers pointés par le paramètre _lpSortCriteria_ sont trop complexes. **SortTable** peut renvoyer MAPI_E_TOO_COMPLEX dans les conditions suivantes. 
    
   - Une opération de tri est demandée pour une colonne de propriétés que l'implémentation ne peut pas trier.
    
   - L'implémentation ne prend pas en charge l'ordre de tri demandé dans le membre **ulOrder** de la structure **SSortOrderSet** . 
    
   - Le nombre de colonnes à trier, tel qu'il est spécifié dans le membre **cSorts** dans **SSortOrderSet**, est plus important que l'implémentation peut gérer.
    
   - Une opération de tri est demandée, comme indiqué par une balise de propriété dans **SSortOrderSet**, en fonction d'une propriété qui n'est pas dans l'ensemble disponible ou actif et l'implémentation ne prend pas en charge le tri sur les propriétés qui ne sont pas dans l'ensemble disponible.
    
   - Une propriété est spécifiée plusieurs fois dans un ordre de tri défini, comme indiqué par plusieurs instances de la même balise de propriété, et l'implémentation ne peut pas effectuer une telle opération de tri.
    
   - Une opération de tri basée sur des colonnes de propriétés à valeurs multiples est demandée à l'aide de MVI_FLAG et l'implémentation ne prend pas en charge le tri sur les propriétés à valeurs multiples. 
    
   - Une balise de propriété pour une propriété dans **SSortOrderSet** spécifie une propriété ou un type que l'implémentation ne prend pas en charge. 
    
   - Une opération de tri autre que celle qui parcourt le tableau à partir de la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) est spécifiée uniquement pour une table de pièces jointes qui prend en charge ce type de tri.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: SortTable** trie les lignes dans un affichage tableau. Bien que certaines tables prennent en charge à la fois le tri standard et le tri par catégorie sur différentes colonnes de clés de tri, les autres tableaux sont plus limités dans leur prise en charge. En règle générale, les fournisseurs de carnets d'adresses ne prennent pas en charge le tri de table. Les fournisseurs de banques de messages prennent généralement en charge le tri dans la mesure où ils conservent l'ordre de tri des dossiers résultant de la création d'une table complète (table sans restrictions). 
  
Certaines tables permettent le tri sur n'importe quelle colonne de tableau. Les autres tables ne le sont pas; les colonnes non incluses dans l'affichage tableau ne sont pas affectées par un appel **SortTable** . Dans certains tableaux, les clés de tri ne doivent être créées qu'avec des colonnes dans le jeu de colonnes actuel de la table. 
  
Une table peut renvoyer MAPI_E_NO_SUPPORT ou MAPI_E_TOO_COMPLEX à partir de **SortTable** lorsqu'elle ne peut pas effectuer une opération de tri. Par ailleurs, il n'est pas garanti que les fournisseurs de magasins respectent l'ordre de tri défini pour les tables de hiérarchie. 
  
Lorsqu'il n'y a aucune colonne dans la structure [SSortOrderSet](ssortorderset.md) vers laquelle pointe le paramètre _lpSortCriteria_ , la table renvoie le jeu de colonnes actuel. L'ordre de tri actuel peut être récupéré en appelant la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) . 
  
Tous les signets d'une table sont invalidés et doivent être supprimés lorsqu'un appel à **SortTable** est effectué et que le signet BOOKMARK_CURRENT qui indique la position actuelle du curseur doit être défini au début du tableau. 
  
Si vous triez sur une colonne qui contient une propriété à valeurs multiples sans l'indicateur MVI_FLAG défini, les valeurs de la colonne sont traitées comme un tuple entièrement ordonné. Une comparaison de deux colonnes à valeurs multiples compare les éléments de colonne dans l'ordre, en signalant la relation entre les colonnes à la première inégalité et ne renvoie l'égalité que si les colonnes comparées contiennent les mêmes valeurs dans le même ordre. Si une colonne comporte moins de valeurs que l'autre, la relation signalée est celle d'une valeur null à l'autre valeur.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

**SortTable** fonctionne de façon synchrone, sauf si vous définissez l'un des indicateurs. Si vous définissez l'indicateur TBL_BATCH, **SortTable** diffère l'opération de tri, sauf si vous demandez les données. Si l'indicateur TBL_ASYNC est défini, **SortTable** fonctionne de manière asynchrone, pouvant renvoyer avant la fin de l'opération. 
  
Appelez la méthode [IMAPITable:: Abort](imapitable-abort.md) pour arrêter une opération asynchrone en cours si votre tri doit être réalisé immédiatement. Si **SortTable** ne peut pas continuer car une ou plusieurs opérations asynchrones sur la table sont en cours, elle renvoie MAPI_E_BUSY. 
  
Pour de meilleures performances, appelez **SetColumns** pour personnaliser le jeu de colonnes de la table et **limiter** le nombre de lignes de la table avant d'appeler **SortTable** pour effectuer le tri. 
  
Chaque fois que **SortTable** échoue, l'ordre de tri qui était en vigueur avant la défaillance est toujours en vigueur. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

