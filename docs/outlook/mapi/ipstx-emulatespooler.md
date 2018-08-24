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
ms.openlocfilehash: 079b54757cfcd5c9b38365abc5a6d901e2b06724
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580718"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit un magasin pour émuler le Gestionnaire de protocole Outlook pour mettre en attente des messages sortants vers un serveur local.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Définissez ce paramètre sur True si la banque locale doit émuler le spouleur ; défini sur False dans le cas contraire. 
    
## <a name="remarks"></a>Remarques

Une banque locale appelle **IPSTX::EmulateSpooler** pour agir comme un gestionnaire de protocole Outlook, les messages en attente dans la file d’attente sortante pour le serveur principal (par exemple, le serveur MSN ou le serveur de AOL) pour le traitement. Le magasin émule un spouleur lors de la synchronisation, puis appelle ces deux méthodes : 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** pour obtenir la sortant de la file d’attente de messages dans le magasin. Cette méthode fonctionne uniquement si la banque émule le Gestionnaire de protocole Outlook. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** pour sécuriser l’accès exclusif à un message dans la file d’attente sortante juste avant l’envoi au serveur. Cette méthode fonctionne uniquement si la banque émule le Gestionnaire de protocole Outlook. Après avoir envoyé le message, le magasin appelle cette méthode pour libérer un accès exclusif au son. 
    
> [!NOTE]
> Depuis Outlook 2002, le Gestionnaire de protocole Outlook remplacé le spouleur MAPI et qu’il est devenu responsable pour les messages sortants en attente pour les serveurs principaux. 
  
## <a name="see-also"></a>Voir aussi



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

