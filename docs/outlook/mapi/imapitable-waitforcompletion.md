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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c7859e033924786e415f9faa9f75021ea47968c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784100"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**S’applique à**: Outlook 
  
Interrompt le traitement jusqu'à ce qu’un ou plusieurs asynchrones opérations en cours sur la table est terminé.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
 _ulTimeout_
  
> [in] Nombre maximal de millisecondes d’attente pour l’opération asynchrone ou les opérations à effectuer. Pour attendre indéfiniment jusqu'à ce que l’exécution se produit, définissez _ulTimeout_ sur 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [entrée, sortie] À l’entrée, un pointeur valide ou valeur NULL. Dans la sortie, si _lpulTableStatus_ est un pointeur valid, il pointe vers le dernier état de la table. Si _lpulTableStatus_ est NULL, aucune information d’état n’est retournée. Si **WaitForCompletion** renvoie une valeur HRESULT échoue, le contenu de _lpulTableStatus_ n’est pas défini. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’opération d’attente a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne gère pas en attente pour l’exécution d’opérations asynchrones.
    
MAPI_E_TIMEOUT 
  
> L’opération asynchrone ou les opérations ne s’est pas terminée dans le délai spécifié.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::WaitForCompletion** interrompt le traitement jusqu'à ce qu’une opération asynchrone actuellement en cours de la table est terminé. **WaitForCompletion** peut autoriser les opérations asynchrones à entièrement terminée ou pour exécuter un certain nombre de millisecondes, comme indiqué par _ulTimeout_, avant d’être interrompu. Pour détecter les opérations asynchrones en cours, appelez la méthode [IMAPITable::GetStatus](imapitable-getstatus.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

