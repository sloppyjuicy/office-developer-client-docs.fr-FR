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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348747"
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

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> dans Pointeur vers le message à verrouiller ou déverrouiller.
    
 _ulLockState_
  
> dans Valeur qui indique si le message doit être verrouillé ou déverrouillé. L'une des valeurs suivantes est valide:
    
MSG_LOCKED 
  
> Le message doit être verrouillé. 
    
MSG_UNLOCKED 
  
> Le message doit être déverrouillé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'état de verrouillage du message a été correctement défini.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore:: SetLockState** verrouille ou déverrouille un message. **SetLockState** ne peut être appelée que par le spouleur MAPI pendant l'envoi du message. 
  
En règle générale, lorsque le spouleur MAPI appelle **SetLockState** pour verrouiller un message, il verrouille uniquement le plus ancien message (c'est-à-dire, le message suivant en file d'attente pour le spouleur MAPI à envoyer). Si le message le plus ancien de la file d'attente attend un fournisseur de transport temporairement indisponible et que le message suivant de la file d'attente utilise un autre fournisseur de transport, le spouleur MAPI peut commencer à traiter le message ultérieur. Elle commence à traiter en verrouillant ce message à l'aide de **SetLockState**.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Une fois que le spouleur MAPI a appelé **SetLockState** avec le paramètre _ULLOCKSTATE_ défini sur MSG_LOCKED, les appels à la méthode [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) pour annuler la transmission du message doivent échouer. 
  
Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message dans votre implémentation **SetLockState** afin que les modifications qui ont été apportées au message avant la réception de l'appel de **SetLockState** soient enregistrées. 
  
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

