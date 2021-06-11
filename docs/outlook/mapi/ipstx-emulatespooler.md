---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438952"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit un magasin local pour émuler le gestionnaire Outlook protocole pour mettre en file d’ensemble les messages sortants sur un serveur.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Définissez ce paramètre sur True si le magasin local doit émuler lepooler ; si ce n’est pas le cas. 
    
## <a name="remarks"></a>Remarques

Un magasin local appelle **IPSTX::EmulateSpooler** pour agir en tant que gestionnaire de protocole Outlook, en stockant les messages dans la file d’attente sortante vers le serveur principal (par exemple, le serveur MSN ou le serveur AOL) pour le traitement. Lors de l’émulation d’unpooler lors de la synchronisation, le magasin appelle ensuite les deux méthodes ci-après : 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store. Cette méthode réussit uniquement si le magasin émule le gestionnaire Outlook protocole. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** pour sécuriser l’accès unique à un message dans la file d’attente sortante juste avant de l’envoyer au serveur. Cette méthode réussit uniquement si le magasin émule le gestionnaire Outlook protocole. Après l’envoi du message, la boutique appelle à nouveau cette méthode pour libérer l’accès unique à celui-ci. 
    
> [!NOTE]
> Depuis Outlook 2002, le gestionnaire de protocole Outlook a remplacé lepooler MAPI et est devenu responsable dupooling des messages sortants sur les serveurs back-end. 
  
## <a name="see-also"></a>Voir aussi



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

