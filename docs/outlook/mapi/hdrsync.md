---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
ms.openlocfilehash: 7918db66ca41ba13b62fea2fa345fc5e5572520d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368838"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour la synchronisation d’un en-tête de message pendant [l’état d’en-tête du message de téléchargement](download-message-header-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a>Membres

 _pupmsg_
  
- [out] Informations pour l’en-tête de message actuel dans la boutique locale.
    
 _todPar_
  
- [out] ID d’entrée pour le dossier parent de l’élément de message.
    
 _pstmReserved_
  
- [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
 _ulFlags_
  
- [in] Indicateurs pour modifier le comportement :
    
- HSF_LOCAL
    
  - [in] L’élément complet réside dans la même boutique locale que l’élément d’en-tête.
    
- HSF_COPYDESTRUCTIVE
    
  -  [in] Optimiser les opérations de copie interne. Cela peut entraîner une perte de données. **HSF_LOCAL** doit être définie. 
    
- HSF_OK
    
  - [in] La synchronisation d’en-tête a réussi. Le client définit cet élément après avoir téléchargé des informations à partir du serveur.
    
     _pmsgFull_
    
  - [in] L’élément de message complet, y compris l’en-tête de message téléchargé à partir du serveur. Voir mapidefs.h pour la définition de type **de LPMESSAGE**. 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[FEID](feid.md)

