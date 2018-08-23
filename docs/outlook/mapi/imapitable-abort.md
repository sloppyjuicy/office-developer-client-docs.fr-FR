---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 68d40a6e152698554fcb88c6f7e5bfd4a7ff0ce3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574005"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Arrête toutes les opérations asynchrones en cours pour la table.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Paramètres

Aucune
  
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Un ou plusieurs des opérations asynchrones ont été arrêtées.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Une opération asynchrone est en cours et ne peut pas être arrêtée ou il a déjà effectué.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::Abort** arrête toute opération asynchrone est en cours. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour savoir si une opération asynchrone est en cours, appelez la méthode [IMAPITable::GetStatus](imapitable-getstatus.md) . 
  
Si **l’abandon** interrompt le traitement d’un appel à la méthode [IMAPITable](imapitable-restrict.md) , l’état de la table sera telle qu’elle était au moment de que l’appel **abandonner** est traité. 
  
Si **abandonner** interrompt le traitement d’un appel à la méthode [IMAPITable::SortTable](imapitable-sorttable.md) , ordre de tri de la table n’est pas affecté et reste tel qu’il était avant l’appel de **SortTable** . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

