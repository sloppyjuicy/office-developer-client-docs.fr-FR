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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a4e924489f2ec656f473f28407d528e9c2ddda5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784251"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**S’applique à**: Outlook 
  
Verrouiller ou déverrouiller un message. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Param�tres

 _lpMessage_
  
> [in] Pointeur vers le message pour verrouiller ou déverrouiller.
    
 _ulLockState_
  
> [in] Une valeur qui indique si le message doit être verrouillé ou déverrouillé. Valide une des valeurs suivantes :
    
MSG_LOCKED 
  
> Le message doit être verrouillé. 
    
MSG_UNLOCKED 
  
> Le message doit être déverrouillé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’état de verrouillage du message a été correctement définie.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::SetLockState** verrouille ou déverrouille un message. **SetLockState** peut être appelée uniquement par le spouleur MAPI pendant qu’il envoie le message. 
  
En règle générale, lorsque le spouleur MAPI appelle **SetLockState** pour verrouiller un message, il est verrouillé uniquement le message le plus ancien (autrement dit, le message suivant en file d’attente pour le spouleur MAPI envoyer). Si le message le plus ancien dans la file d’attente est en attente d’un fournisseur de transport temporairement indisponible et le message suivant dans la file d’attente utilise un fournisseur de transport différents, le spouleur MAPI permettre commencer à traiter le message ultérieure. Il commence le traitement par le verrouillage de ce message à l’aide de **SetLockState**.
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Une fois que le spouleur MAPI a appelé **SetLockState** avec le paramètre _ulLockState_ défini sur MSG_LOCKED, les appels à la méthode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour annuler la transmission du message doivent échouer. 
  
Appelez la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message dans votre implémentation **SetLockState** afin que les modifications qui ont été apportées au message avant l’appel **SetLockState** a été reçue. 
  
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

