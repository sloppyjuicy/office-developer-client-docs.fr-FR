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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 51c239897e5e225a0765f78404526e2836371f30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567901"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Reconstruit l’état actuel de développés ou réduit d’une table, voir l’aide de données qui a été enregistrées par un appel antérieur à la méthode [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) . 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
 _cbCollapseState_
  
> [in] Nombre d’octets de la structure vers laquelle pointe le paramètre _pbCollapseState_ . 
    
 _pbCollapseState_
  
> [in] Pointeur vers les structures contenant les données nécessaires à la recréation de l’affichage tableau.
    
 _lpbkLocation_
  
> [out] Pointeur vers un signet qui identifie la ligne dans la table à laquelle l’état réduit ou développé doit être reconstruite. Ce signet et la clé d’instance passé dans le paramètre _lpbInstanceKey_ dans l’appel à [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identifient la même ligne. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’état de la table par catégorie a été correctement recréé.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche l’opération de démarrage. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Le tableau n’a pas pu terminer la reconstruction de l’affichage réduit ou développé.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::SetCollapseState** rétablit l’état développé ou réduit de l’affichage tableau. **SetCollapseState** et **GetCollapseState** collaborent comme suit : 
  
1. Lorsque l’état d’une table, voir va changer, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) est appelée pour enregistrer toutes les données relatives à l’état avant la modification. 
    
2. Pour restaurer l’affichage de la table à son état enregistré, **SetCollapseState** est appelée. Les données enregistrées par **GetCollapseState** sont transmises à **SetCollapseState**. **SetCollapseState** est en mesure d’utiliser ces données pour restaurer l’état. 
    
3. **SetCollapseState** retourne, sous la forme d’un paramètre de sortie, un signet qui identifie la même ligne que la clé d’instance passée comme entrée pour **GetCollapseState**.
    
Pour plus d’informations sur les tables, voir, consultez [tri et catégorisation](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Vous êtes responsable de vérifier que l’ordre de tri et les restrictions sont exactement les mêmes qu’elles étaient au moment de l’appel **GetCollapseState** . Si une modification a été apportée, **SetCollapseState** ne doit pas être appelée, car le résultat est imprévisible. Cela peut se produire si, par exemple, un client appelle **GetCollapseState** , puis **SortTable** pour modifier la clé de tri avant d’appeler **SetCollapseState**. Pour plus de sécurité, vérifiez que les données enregistrées sont toujours valides avant de procéder à la restauration. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour appeler **SetCollapseState**, vous devez avez précédemment appelé **GetCollapseState**. L’ordre de tri établir les catégories doit être la même pour les deux méthodes. Si les ordres de tri diffèrent, le résultat de l’opération **SetCollapseState** est imprévisible. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

