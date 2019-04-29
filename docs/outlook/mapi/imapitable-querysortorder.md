---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407549"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère l'ordre de tri actuel d'une table.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Paramètres

 _lppSortCriteria_
  
> remarquer Pointeur vers un pointeur vers la structure [SSortOrderSet](ssortorderset.md) qui contient l'ordre de tri actuel. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'ordre de tri actuel a été renvoyé.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de récupération de l'ordre de tri. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: QuerySortOrder** extrait l'ordre de tri actuel d'une table. Les ordres de tri sont décrits par une structure [SSortOrderSet](ssortorderset.md) . 
  
- Le membre **cSorts** de la structure **SSortOrderSet** peut être défini sur zéro si: 
    
- Le tableau n'est pas trié.
    
- Il n'existe aucune information sur la façon dont le tableau est trié.
    
- La structure **SSortOrderSet** n'est pas appropriée pour décrire l'ordre de tri. 
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si un appel est passé à votre méthode [IMAPITable:: SortTable](imapitable-sorttable.md) avec une structure **SSortOrderSet** contenant zéro colonne dans la clé de tri, supprimez l'ordre de tri actuel et appliquez l'ordre par défaut, s'il en existe un. Dans les appels suivants à **QuerySortOrder**, vous pouvez choisir de renvoyer zéro ou plusieurs colonnes pour la clé de tri. Vous pouvez renvoyer plus de colonnes que ce qui est dans la vue actuelle.
  
Pour plus d'informations sur le tri, reportez-vous à la rubrique [Tri et catégorisation](sorting-and-categorization.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

