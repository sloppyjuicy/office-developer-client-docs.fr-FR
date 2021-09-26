---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bc55f579e7d161d9899d29e5c8239db347980c53
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630683"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Arrête toutes les opérations asynchrones en cours pour la table.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Une ou plusieurs opérations asynchrones ont été arrêtées.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Une opération asynchrone est en cours et ne peut pas être arrêtée ou elle est déjà terminée.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::Abort** arrête toute opération asynchrone en cours. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour savoir si une opération asynchrone est en cours, appelez la méthode [IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
Si **Abort** interrompt le traitement d’un appel à la méthode [IMAPITable::Restrict,](imapitable-restrict.md) l’état de la table sera tel qu’il était au moment du traitement de l’appel d’abandon.  
  
Si **Abort** interrompt le traitement d’un appel à la méthode [IMAPITable::SortTable,](imapitable-sorttable.md) l’ordre de tri de la table n’est pas affecté et reste tel qu’il était avant l’appel **sortTable.** 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

