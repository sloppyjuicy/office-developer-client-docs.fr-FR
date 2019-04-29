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
  
Définit une banque locale pour émuler le gestionnaire de protocoles Outlook afin de spouler les messages sortants vers un serveur.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  dans Définissez ce paramètre sur true si le magasin local doit émuler le spouleur; Définissez-la sur false dans le cas contraire. 
    
## <a name="remarks"></a>Remarques

Un magasin local appelle **IPSTX:: EmulateSpooler** pour agir en tant que gestionnaire de protocoles Outlook, en spoule les messages de la file d'attente sortante vers le serveur principal (par exemple, le serveur MSN ou le serveur AOL) pour traitement. Émulation d'un spouleur pendant la synchronisation, le magasin appelle les deux méthodes suivantes: 
  
1. **[IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** pour obtenir la file d'attente de messages sortante dans la Banque. Cette méthode ne réussit que si la Banque émule le gestionnaire de protocoles Outlook. 
    
2. **[IMsgStore:: SetLockState](imsgstore-setlockstate.md)** pour sécuriser l'accès exclusif à un message dans la file d'attente sortante juste avant de l'envoyer au serveur. Cette méthode ne réussit que si la Banque émule le gestionnaire de protocoles Outlook. Après l'envoi du message, le magasin appelle de nouveau cette méthode pour lui libérer un accès exclusif. 
    
> [!NOTE]
> Depuis Outlook 2002, le gestionnaire de protocoles Outlook remplace le spouleur MAPI et est devenu responsable de la mise en file d'attente des messages sortants vers les serveurs principaux. 
  
## <a name="see-also"></a>Voir aussi



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

