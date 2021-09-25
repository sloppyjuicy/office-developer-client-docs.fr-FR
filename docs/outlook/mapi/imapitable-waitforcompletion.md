---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6b726bbf32e6c97566471a6ae6be4c33aa7e92d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575735"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Suspend le traitement jusqu’à ce qu’une ou plusieurs opérations asynchrones en cours sur la table soient terminées.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> Réservé ; doit être zéro.
    
 _ulTimeout_
  
> [in] Nombre maximal de millisecondes à attendre pour que l’opération ou les opérations asynchrones se terminent. Pour attendre indéfiniment que l’achèvement se produise, définissez  _ulTimeout_ sur 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] Lors de l’entrée, pointeur valide ou NULL. En sortie, si  _lpulTableStatus_ est un pointeur valide, il pointe vers l’état le plus récent du tableau. Si  _lpulTableStatus a_ la valeur NULL, aucune information d’état n’est renvoyée. Si **WaitForCompletion** renvoie une valeur HRESULT infructueuse, le contenu de  _lpulTableStatus_ n’est pas définie. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération d’attente a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne prend pas en charge l’attente de la fin des opérations asynchrones.
    
MAPI_E_TIMEOUT 
  
> L’opération asynchrone ou les opérations ne se sont pas terminées dans l’heure spécifiée.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::WaitForCompletion** suspend le traitement jusqu’à ce que toutes les opérations asynchrones en cours pour la table soient terminées. **WaitForCompletion** peut permettre aux opérations asynchrones soit de se terminer entièrement, soit de s’exécuter pendant un certain nombre de millisecondes, comme indiqué par  _ulTimeout_, avant d’être interrompues. Pour détecter les opérations asynchrones en cours, appelez la méthode [IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

