---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342783"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour la synchronisation d'un en-tête de message lors de l' [État d'en-tête de message de téléchargement](download-message-header-state.md).
  
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
  
- remarquer Informations de l'en-tête de message actuel dans le magasin local.
    
 _feidPar_
  
- remarquer ID d'entrée du dossier parent de l'élément de message.
    
 _pstmReserved_
  
- [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
 _ulFlags_
  
- dans Indicateurs permettant de modifier le comportement:
    
- HSF_LOCAL
    
  - dans L'élément complet réside dans le même magasin local que l'élément d'en-tête.
    
- HSF_COPYDESTRUCTIVE
    
  -  dans Optimiser les opérations de copie interne. Cela peut entraîner une perte de données. **HSF_LOCAL** doit être défini. 
    
- HSF_OK
    
  - dans La synchronisation d'en-tête a réussi. Le client définit cet élément après avoir téléchargé des informations à partir du serveur.
    
     _pmsgFull_
    
  - dans Élément de message complet incluant l'en-tête de message téléchargé à partir du serveur. Voir mapidefs. h pour la définition de type de **LPMESSAGE**. 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[FEID](feid.md)

