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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 46a87a6eb5c80244c04ae6257cd4441b8797ba36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784103"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**S’applique à**: Outlook 
  
La méthode **IMAPITable::SortTable** trie les lignes du tableau, en fonction de tri critères. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_lpSortCriteria_
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui contient les critères de tri à appliquer. Passage d’une structure **SSortOrderSet** qui contient zéro colonnes indique que le tableau n’a pas à trier selon un ordre particulier. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le minutage de l’opération **IMAPITable::SortTable** . Les indicateurs suivants peuvent être définis : 
    
TBL_ASYNC 
  
> Démarre l’opération asynchrone et renvoie avant que l’opération est terminée.
    
TBL_BATCH 
  
> Diffère de la fin de l’ordre de tri jusqu'à ce que les données dans le tableau sont requises.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’opération de tri a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche l’opération de tri de démarrage. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne gère pas le type de tri demandé.
    
MAPI_E_TOO_COMPLEX 
  
> Le tableau ne peut pas effectuer l’opération car les critères de tri particulier vers laquelle pointe le paramètre _lpSortCriteria_ est trop complexe. **SortTable** peut renvoyer MAPI_E_TOO_COMPLEX dans les conditions suivantes. 
    
   - Une opération de tri est demandée pour une colonne de propriété que l’implémentation ne peut pas trier.
    
   - L’implémentation ne gère pas l’ordre de tri demandée dans le membre **ulOrder** de la structure **SSortOrderSet** . 
    
   - Le nombre de colonnes à trier, tel que spécifié dans le membre **cSorts** dans **SSortOrderSet**, est plus importante que l’implémentation peut gérer.
    
   - Une opération de tri est demandée, comme indiqué par une balise de propriété **SSortOrderSet**, basée sur une propriété qui n’est pas dans l’ensemble actif ou disponible et l’implémentation ne gère pas le tri sur les propriétés pas dans l’ensemble disponible.
    
   - Une propriété est spécifiée plusieurs fois dans un jeu d’ordre de tri, comme indiqué par plusieurs instances de la même balise de propriété, et l’implémentation ne peut pas effectuer une opération de tri de ce type.
    
   - Une opération de tri basée sur les colonnes de la propriété à valeurs multiples est demandée à l’aide de MVI_FLAG et l’implémentation ne gère pas le tri sur les propriétés à valeurs multiples. 
    
   - Une balise de propriété pour une propriété dans **SSortOrderSet** spécifie une propriété ou un type de l’implémentation ne prenant pas en charge. 
    
   - Une opération de tri autre que celui qui s’effectue par le biais de la table à partir de la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) transférer est spécifiée uniquement pour une table de pièce jointe qui prend en charge ce type de tri.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::SortTable** trie les lignes dans un affichage tableau. Tandis que certaines tables prend en charge le tri sur plusieurs colonnes de clé de tri standard et par catégorie, les autres tables sont plus limitées dans leur prise en charge. Fournisseurs de carnet d’adresses, ne prennent pas charge tri des tableaux. Fournisseurs de banque de messages prennent généralement en charge le tri dans la mesure où ils conservent l’ordre de tri des dossiers qui se produit lorsqu’une table complète (il s’agit d’une table sans restriction) est triée. 
  
Certaines tables autorisent le tri est effectué sur n’importe quelle colonne du tableau. Autres tables mais pas ; colonnes non inclus dans l’affichage tableau ne sont pas affectés par un appel **SortTable** . Certaines tables nécessitent que les clés de tri générés uniquement avec les colonnes dans le jeu de colonne en cours. 
  
Un tableau peut retourner MAPI_E_NO_SUPPORT ou MAPI_E_TOO_COMPLEX à partir de **SortTable** lorsqu’il ne peut pas effectuer une opération de tri. En outre, les fournisseurs de magasins ne sont pas nécessairement de respecter l’ordre de tri spécifié pour les tables de hiérarchie. 
  
Lorsqu’il n’y a aucune colonne dans la structure [SSortOrderSet](ssortorderset.md) désignée par le paramètre _lpSortCriteria_ , la table renvoie l’ensemble actuel de la colonne. L’ordre de tri actuel peut être récupéré en appelant la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) de la table. 
  
Tous les signets pour une table sont invalidés et doivent être supprimés lorsqu’un appel à **SortTable** est effectué et le signet BOOKMARK_CURRENT qui indique l’emplacement du curseur, doit être défini au début de la table. 
  
Si vous triez sur une colonne qui contient une propriété à valeurs multiples sans l’indicateur MVI_FLAG est défini, les valeurs de la colonne sont considérés comme un tuple complètement triée. Une comparaison de deux colonnes à valeurs multiples compare les éléments de la colonne dans l’ordre, la relation entre les colonnes de la première inégalité, de création de rapports et renvoie l’égalité uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre. Si une colonne a moins de valeurs à l’autre, la relation signalée est celui d’une valeur null à l’autre valeur.
  
## <a name="notes-to-callers"></a>Notes aux appelants

**SortTable** fonctionne de manière synchrone, sauf si vous définissez un des indicateurs. Si vous définissez l’indicateur TBL_BATCH, **SortTable** diffère de l’opération de tri, sauf si vous demandez les données. Si l’indicateur TBL_ASYNC est défini, **SortTable** fonctionne de manière asynchrone, potentiellement renvoi avant la fin de l’opération. 
  
Appelez la méthode [IMAPITable::Abort](imapitable-abort.md) pour arrêter une opération asynchrone en cours si le tri doit être effectué immédiatement. Si **SortTable** ne peut pas continuer car un ou plusieurs des opérations asynchrones dans le tableau sont en cours, elle renvoie MAPI_E_BUSY. 
  
Pour optimiser les performances, appelez **SetColumns** pour personnaliser l’ensemble de colonnes de la table et **Restrict** pour limiter le nombre de lignes dans le tableau avant d’appeler **SortTable** pour effectuer le tri. 
  
Chaque fois que **SortTable** échoue, l’ordre de tri qui était en vigueur avant la défaillance est toujours en vigueur. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

