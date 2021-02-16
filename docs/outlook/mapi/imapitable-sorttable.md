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
  
La **méthode IMAPITable::SortTable** trie les lignes du tableau, selon les critères de tri. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_lpSortCriteria_
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui contient les critères de tri à appliquer. La transmission **d’une structure SSortOrderSet** qui contient zéro colonne indique que le tableau n’a pas besoin d’être trié dans un ordre particulier. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le minutage de **l’opération IMAPITable::SortTable.** Les indicateurs suivants peuvent être définies : 
    
TBL_ASYNC 
  
> Démarre l’opération de manière asynchrone et la renvoie avant la fin de l’opération.
    
TBL_BATCH 
  
> Reporte la fin du tri jusqu’à ce que les données de la table soient requises.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de tri a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de tri. L’opération en cours doit être autorisée ou arrêtée.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne prend pas en charge le type de tri demandé.
    
MAPI_E_TOO_COMPLEX 
  
> La table ne peut pas effectuer l’opération, car les critères de tri spécifiques pointés par  _le paramètre lpSortCriteria_ sont trop complexes. **SortTable** peut renvoyer MAPI_E_TOO_COMPLEX dans les conditions suivantes. 
    
   - Une opération de tri est demandée pour une colonne de propriété que l’implémentation ne peut pas trier.
    
   - L’implémentation ne prend pas en charge l’ordre de tri demandé dans le membre **ulOrder** de la structure **SSortOrderSet.** 
    
   - Le nombre de colonnes à trier, tel que spécifié dans le membre **cSorts** dans **SSortOrderSet,** est supérieur à ce que l’implémentation peut gérer.
    
   - Une opération de tri est demandée, comme indiqué par une balise de propriété dans **SSortOrderSet,** basée sur une propriété qui n’est pas dans le jeu disponible ou actif et l’implémentation ne prend pas en charge le tri sur les propriétés qui ne sont pas dans le jeu disponible.
    
   - Une propriété est spécifiée plusieurs fois dans un jeu d’ordre de tri, comme indiqué par plusieurs instances de la même balise de propriété, et l’implémentation ne peut pas effectuer cette opération de tri.
    
   - Une opération de tri basée sur des colonnes de propriétés à valeurs multiples est demandée à l’aide de MVI_FLAG et l’implémentation ne prend pas en charge le tri sur les propriétés à valeurs multiples. 
    
   - Une balise de propriété pour une propriété **dans SSortOrderSet** spécifie une propriété ou un type que l’implémentation ne prend pas en charge. 
    
   - Une opération de tri autre qu’une opération de tri qui passe par le tableau à partir de la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) est spécifiée uniquement pour une table de pièces jointes qui prend en charge ce type de tri.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::SortTable** trie les lignes dans un affichage Tableau. Alors que certains tableaux peuvent à la fois être triés standard et catégorisés sur différentes colonnes de clé de tri, d’autres tableaux sont plus limités dans leur prise en charge. Les fournisseurs de carnets d’adresses ne peuvent généralement pas prendre en charge le tri des tables. Les fournisseurs de magasins de messages prend généralement en charge le tri dans la mesure où ils conservent l’ordre de tri des dossiers qui en résulte lorsqu’un tableau complet (un tableau sans restrictions) est trié. 
  
Certains tableaux permettent le tri sur n’importe quelle colonne de tableau. Les autres tables ne le font pas ; les colonnes non incluses dans l’affichage Tableau ne sont pas affectées par un **appel SortTable.** Certains tableaux exigent que les clés de tri ne soient construites qu’avec les colonnes du jeu de colonnes actuel du tableau. 
  
Un tableau peut renvoyer des MAPI_E_NO_SUPPORT ou des MAPI_E_TOO_COMPLEX **sortTable** lorsqu’il ne peut pas effectuer une opération de tri. En outre, il n’est pas garanti que les fournisseurs de magasins respectent l’ordre de tri spécifié pour les tables hiérarchiques. 
  
Lorsqu’il n’y a aucune colonne dans la structure [SSortOrderSet](ssortorderset.md) pointée par le paramètre  _lpSortCriteria,_ le tableau renvoie le jeu de colonnes actuel. L’ordre de tri actuel peut être récupéré en appelant la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) de la table. 
  
Tous les signets d’une table sont invalidés et doivent être supprimés lorsqu’un appel à **SortTable** est effectué, et le signet BOOKMARK_CURRENT qui indique la position actuelle du curseur doit être placé au début du tableau. 
  
Si vous triez sur une colonne qui contient une propriété à valeurs multiples sans l’indicateur MVI_FLAG, les valeurs de la colonne sont traitées comme un tuple entièrement trié. Une comparaison de deux colonnes à valeurs multiples compare les éléments de colonne dans l’ordre, en signalant la relation entre les colonnes à la première égalité et renvoie l’égalité uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre. Si une colonne a moins de valeurs que l’autre, la relation signalée est celle d’une valeur null par rapport à l’autre valeur.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

**SortTable** fonctionne de manière synchrone, sauf si vous définissez l’un des indicateurs. Si vous définissez l’TBL_BATCH, **SortTable** reporte l’opération de tri, sauf si vous demandez les données. Si l TBL_ASYNC est définie, **SortTable** fonctionne de manière asynchrone, ce qui peut renvoyer le résultat avant la fin de l’opération. 
  
Appelez la [méthode IMAPITable::Abort](imapitable-abort.md) pour arrêter une opération asynchrone en cours si votre tri doit être effectué immédiatement. Si **SortTable ne** peut pas continuer parce qu’une ou plusieurs opérations asynchrones sur la table sont en cours, elle renvoie MAPI_E_BUSY. 
  
Pour de meilleures performances, appelez **SetColumns** pour  personnaliser le jeu de colonnes du tableau et limitez le nombre de lignes dans le tableau avant d’appeler **SortTable** pour effectuer le tri. 
  
Chaque **fois que SortTable** échoue, l’ordre de tri qui était en vigueur avant l’échec est toujours en vigueur. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

