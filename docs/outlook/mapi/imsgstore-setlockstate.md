---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423628"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Verrouille ou déverrouille un message. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Pointeur vers le message à verrouiller ou déverrouiller.
    
 _ulLockState_
  
> [in] Valeur qui indique si le message doit être verrouillé ou déverrouillé. L’une des valeurs suivantes est valide :
    
MSG_LOCKED 
  
> Le message doit être verrouillé. 
    
MSG_UNLOCKED 
  
> Le message doit être déverrouillé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état de verrouillage du message a été correctement définie.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::SetLockState** verrouille ou déverrouille un message. **SetLockState peut** être appelé uniquement par lepooler MAPI lors de l’envoi du message. 
  
En règle générale, lorsque lepooler MAPI appelle **SetLockState** pour verrouiller un message, il verrouille uniquement le message le plus ancien (autrement dit, le message suivant mis en file d’attente pour que lepooler MAPI envoie). Si le message le plus ancien de la file d’attente attend un fournisseur de transport temporairement indisponible et que le message suivant dans la file d’attente utilise un autre fournisseur de transport, lepooler MAPI peut commencer à traiter le message ultérieur. Il commence le traitement en verrouiller ce message à l’aide **de SetLockState**.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Une fois que lepooler MAPI a appelé **SetLockState** avec le paramètre  _ulLockState_ définie sur MSG_LOCKED, les appels à la méthode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour annuler la transmission du message doivent échouer. 
  
Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message dans votre implémentation **SetLockState** afin que toutes les modifications apportées au message avant la réception de l’appel **SetLockState** soient enregistrées. 
  
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

