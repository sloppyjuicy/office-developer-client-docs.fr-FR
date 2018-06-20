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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b5eb671be022a6c3aa22e66f68386691fe23b275
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784088"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**S’applique à**: Outlook 
  
Récupère l’ordre de tri en cours pour une table.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Paramètres

 _lppSortCriteria_
  
> [out] Pointeur vers un pointeur vers la structure [SSortOrderSet](ssortorderset.md) maintenant l’ordre de tri en cours. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’ordre de tri en cours a été renvoyée avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche l’opération de récupération d’ordre de tri de démarrer. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::QuerySortOrder** récupère l’ordre de tri en cours pour une table. Ordres de tri sont décrits avec une structure [SSortOrderSet](ssortorderset.md) . 
  
- Le membre **cSorts** de la structure **SSortOrderSet** peut être défini sur zéro si : 
    
- Le tableau n’est pas trié.
    
- Il n’existe pas d’informations sur la façon dont la table est triée.
    
- La structure **SSortOrderSet** n’est pas appropriée pour la description de l’ordre de tri. 
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si un appel est effectué à votre méthode [IMAPITable::SortTable](imapitable-sorttable.md) avec une structure **SSortOrderSet** contenant zéro colonnes dans la clé de tri, supprimez l’ordre de tri en cours et appliquer l’ordre par défaut, le cas échéant. Dans les appels suivants à **QuerySortOrder**, vous pouvez choisir s’il faut renvoyer zéro ou plusieurs colonnes de la clé de tri. Vous pouvez retourner plus de colonnes que dans la vue actuelle.
  
Pour plus d’informations sur le tri, voir [tri et catégorisation](sorting-and-categorization.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

