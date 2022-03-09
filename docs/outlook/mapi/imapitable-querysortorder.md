---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
ms.openlocfilehash: 49154d9beceefa20776ba01a169df3d062cf8e9c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378645"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait l’ordre de tri actuel d’un tableau.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Paramètres

 _lppSortCriteria_
  
> [out] Pointeur vers un pointeur vers la structure [SSortOrderSet](ssortorderset.md) qui détient l’ordre de tri actuel. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’ordre de tri actuel a été renvoyé avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de récupération de l’ordre de tri. L’opération en cours doit être autorisée ou arrêtée.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::QuerySortOrder** récupère l’ordre de tri actuel d’une table. Les ordres de tri sont décrits avec [une structure SSortOrderSet](ssortorderset.md) . 
  
- Le **membre cSorts** de la structure **SSortOrderSet** peut être définie sur zéro si : 
    
- Le tableau n’est pas trié.
    
- Il n’existe aucune information sur la façon dont le tableau est trié.
    
- La structure **SSortOrderSet** n’est pas appropriée pour décrire l’ordre de tri. 
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si un appel est effectué à votre méthode [IMAPITable::SortTable](imapitable-sorttable.md) avec une structure **SSortOrderSet** contenant zéro colonne dans la clé de tri, supprimez l’ordre de tri actuel et appliquez l’ordre par défaut, s’il en existe un. Dans les appels **suivants à QuerySortOrder**, vous pouvez choisir de renvoyer zéro ou plusieurs colonnes pour la clé de tri. Vous pouvez renvoyer plus de colonnes que dans l’affichage actuel.
  
Pour plus d’informations sur le tri, voir [Tri et catégorisation](sorting-and-categorization.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

