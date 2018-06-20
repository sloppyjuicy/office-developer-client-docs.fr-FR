---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787439"
---
# <a name="upmsg"></a>UPMSG

**S’applique à**: Outlook 
  
Informations de téléchargement d’un élément Outlook pendant la [Télécharger l’état du message](upload-message-state.md).
  
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
  
> [out] / [in] indicateurs pour déterminer le comportement approprié lors du téléchargement. 
    
  - UPM_ASSOC
    
    - [out] Élément est associé.
    
  - UPM_NEW
    
    - [out] Nouvel élément. 
    
  - UPM_MOV
    
    - [out] Élément a été déplacé.
    
  - UPM_MOD_PROPS
    
    - [out] Propriétés des éléments ont été modifiées.
    
  - UPM_HEADER
    
    - [out] Item est un en-tête de message.
    
  - UPM_OK
    
    - [in] Téléchargement a réussi. Le client définit après le chargement des informations sur le serveur.
    
  - UPM_MOVED
    
    - [in] Élément a été déplacé avec succès.
    
  - UPM_COMMIT
    
    - [in] Valider : état du téléchargement maintenant.
    
  - UPM_DELETE
    
    - [in] Supprimer l’élément maintenant.
    
  - UPM_SAVE
    
    - [in] Enregistrez les modifications apportées à l’élément.
    
_pMsg_
  
> [out] Ouvrir l’élément objet. Voir mapidefs.h pour la définition du type de **LPMESSAGE**. 
    
_meid_
  
> [out] ID d’entrée de l’élément.
    
_binReserved1_
  
> [in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_binReserved2_
  
> [in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_feid_
  
> [out] ID d’entrée du dossier source, si l’élément a été déplacé.
    
_binChg_
  
> [out] Modifier la clé de l’élément de destination, si l’élément a été déplacé. Voir mapidefs.h pour la définition du type de **SBinary**. 
    
_binPcl_
  
> [out] Modifier la liste de l’élément de destination, si l’élément a été déplacé. Voir mapidefs.h pour la définition du type de **SBinary**. 
    
_skeySrc_
  
> [out] Clé de la source de l’élément source, si l’élément a été déplacé.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

