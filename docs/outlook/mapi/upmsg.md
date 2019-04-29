---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427268"
---
# <a name="upmsg"></a>UPMSG

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le téléchargement d'un élément Outlook lors de l' [État du message de chargement](upload-message-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a>Membres

 _ulFlags_
  
> [out]/[in] indicateurs pour déterminer le comportement approprié pendant le chargement. 
    
  - UPM_ASSOC
    
    - remarquer L'élément est associé.
    
  - UPM_NEW
    
    - remarquer Nouvel élément. 
    
  - UPM_MOV
    
    - remarquer L'élément a été déplacé ici.
    
  - UPM_MOD_PROPS
    
    - remarquer Les propriétés de l'élément ont été modifiées.
    
  - UPM_HEADER
    
    - remarquer L'élément est un en-tête de message.
    
  - UPM_OK
    
    - dans Le chargement a réussi. Le client le définit après avoir téléchargé des informations sur le serveur.
    
  - UPM_MOVED
    
    - dans L'élément a été déplacé.
    
  - UPM_COMMIT
    
    - dans Valider l'état du chargement maintenant.
    
  - UPM_DELETE
    
    - dans Supprimez l'élément maintenant.
    
  - UPM_SAVE
    
    - dans Enregistrer les modifications apportées à l'élément.
    
_PMSG_
  
> remarquer Ouvrir un objet d'élément. Voir mapidefs. h pour la définition de type de **LPMESSAGE**. 
    
_MEID_
  
> remarquer ID d'entrée de l'élément.
    
_binReserved1_
  
> dans Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge. 
    
_binReserved2_
  
> dans Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge. 
    
_feid_
  
> remarquer ID d'entrée du dossier source, si l'élément a été déplacé.
    
_binChg_
  
> remarquer Modifier la clé de l'élément de destination, si l'élément a été déplacé. Voir mapidefs. h pour la définition de type de **SBinary**. 
    
_binPcl_
  
> remarquer Modifier la liste de l'élément de destination, si l'élément a été déplacé. Voir mapidefs. h pour la définition de type de **SBinary**. 
    
_skeySrc_
  
> remarquer Clé source de l'élément source, si l'élément a été déplacé.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

