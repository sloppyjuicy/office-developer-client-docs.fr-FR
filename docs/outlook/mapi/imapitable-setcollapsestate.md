---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328832"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Reconstruit l'état développé ou réduit actuel d'une table catégorisée à l'aide des données qui ont été enregistrées par un appel antérieur à la méthode [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) . 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> MSR doit être égal à zéro.
    
 _cbCollapseState_
  
> dans Nombre d'octets dans la structure vers laquelle pointe le paramètre _pbCollapseState_ . 
    
 _pbCollapseState_
  
> dans Pointeur vers les structures contenant les données nécessaires à la régénération de la vue de table.
    
 _lpbkLocation_
  
> remarquer Pointeur vers un signet identifiant la ligne du tableau à laquelle l'État réduit ou développé doit être reconstruit. Ce signet et la clé d'instance transmis dans le paramètre _lpbInstanceKey_ dans l'appel de [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) identifient la même ligne. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'état de la table classée a été reconstruit avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Le tableau n'a pas pu finir de recréer l'affichage réduit ou développé.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: SetCollapseState** rétablit l'état développé ou réduit de l'affichage tableau. **SetCollapseState** et **GetCollapseState** fonctionnent ensemble comme suit: 
  
1. Lorsque l'état d'une table classée est sur le paragraphe de la modification, la méthode [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) est appelée pour enregistrer toutes les données relatives à l'état avant la modification. 
    
2. Pour restaurer l'état enregistré de la table, **SetCollapseState** est appelé. Les données enregistrées par **GetCollapseState** sont transmises à **SetCollapseState**. **SetCollapseState** est en mesure d'utiliser ces données pour restaurer l'État. 
    
3. **SetCollapseState** renvoie comme paramètre de sortie un signet qui identifie la même ligne que la clé d'instance passée à **GetCollapseState**.
    
Pour plus d'informations sur les tables classées, reportez-vous à la rubrique [Tri et catégorisation](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous êtes chargé de vérifier que l'ordre de tri et les restrictions sont exactement les mêmes qu'au moment de l'appel **GetCollapseState** . Si une modification a été apportée, **SetCollapseState** ne doit pas être appelé car les résultats peuvent être imprévisibles. Cela peut se produire si, par exemple, un client appelle **GetCollapseState** , puis **SortTable** pour modifier la clé de tri avant d'appeler **SetCollapseState**. Pour être sûr, vérifiez que les données enregistrées sont toujours valides avant de procéder à la restauration. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour appeler **SetCollapseState**, vous devez avoir précédemment appelé **GetCollapseState**. L'ordre de tri établissant les catégories doit être le même pour les deux méthodes. Si les ordres de tri diffèrent, les résultats de l'opération **SetCollapseState** sont imprévisibles. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

