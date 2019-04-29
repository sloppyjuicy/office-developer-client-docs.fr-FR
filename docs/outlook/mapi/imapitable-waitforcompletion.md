---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407059"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Interrompt le traitement jusqu'à ce qu'une ou plusieurs opérations asynchrones en cours sur la table soient terminées.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> MSR doit être égal à zéro.
    
 _ulTimeout_
  
> dans Nombre maximal de millisecondes d'attente de l'opération asynchrone ou des opérations à effectuer. Pour attendre indéfiniment jusqu'à la fin de l'opération, définissez _ulTimeout_ sur 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] À l'entrée, soit un pointeur valide, soit NULL. Lors de la sortie, si _lpulTableStatus_ est un pointeur valide, il pointe vers l'état le plus récent de la table. Si _lpulTableStatus_ a la valeur null, aucune information d'État n'est renvoyée. Si **WaitForCompletion** renvoie une valeur HRESULT qui ne réussit pas, le contenu de _lpulTableStatus_ n'est pas défini. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération d'attente a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne prend pas en charge l'exécution des opérations asynchrones.
    
MAPI_E_TIMEOUT 
  
> L'opération asynchrone ou les opérations ne se sont pas terminées dans le temps imparti.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: WaitForCompletion** interrompt le traitement jusqu'à ce que toutes les opérations asynchrones actuellement en cours pour la table soient terminées. **WaitForCompletion** permet aux opérations asynchrones d'effectuer entièrement ou d'exécuter un certain nombre de millisecondes, comme indiqué par _ulTimeout_, avant d'être interrompue. Pour détecter les opérations asynchrones en cours, appelez la méthode [IMAPITable:: GetStatus](imapitable-getstatus.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

