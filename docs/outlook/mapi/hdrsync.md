---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 261a59e628320f384deeb760ba71c9c0386cfde6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576042"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Informations pour la synchronisation d’un en-tête de message au cours de l' [état d’en-tête de message du téléchargement](download-message-header-state.md).
  
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

## <a name="members"></a>Members

 _pupmsg_
  
- [out] Informations de l’en-tête du message en cours dans le magasin local.
    
 _feidPar_
  
- [out] ID d’entrée pour le dossier parent de l’élément de message.
    
 _pstmReserved_
  
- [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
 _ulFlags_
  
- [in] Indicateurs pour modifier le comportement :
    
- HSF_LOCAL
    
  - [in] Élément complet réside dans le même magasin local en tant que l’élément d’en-tête.
    
- HSF_COPYDESTRUCTIVE
    
  -  [in] Optimiser les opérations de copie interne. Cela peut entraîner une perte de données. **HSF_LOCAL** doit être défini. 
    
- HSF_OK
    
  - [in] La réussite de la synchronisation d’en-tête. Le client définit après le téléchargement des informations à partir du serveur.
    
     _pmsgFull_
    
  - [in] L’élément complet y compris l’en-tête de message téléchargé à partir du serveur. Voir mapidefs.h pour la définition du type de **LPMESSAGE**. 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[FEID](feid.md)

