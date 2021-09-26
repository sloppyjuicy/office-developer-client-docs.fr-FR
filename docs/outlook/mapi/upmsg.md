---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d615084e2fc379925f53d08a2dd8ddbe538111ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619511"
---
# <a name="upmsg"></a>UPMSG

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le chargement d’un Outlook pendant [l’état de chargement du message.](upload-message-state.md)
  
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
  
> [out]/[in] Indicateurs pour déterminer le comportement approprié pendant le chargement. 
    
  - UPM_ASSOC
    
    - [out] L’élément est associé.
    
  - UPM_NEW
    
    - [out] Nouvel élément. 
    
  - UPM_MOV
    
    - [out] L’élément a été déplacé ici.
    
  - UPM_MOD_PROPS
    
    - [out] Les propriétés d’élément ont été modifiées.
    
  - UPM_HEADER
    
    - [out] L’élément est un en-tête de message.
    
  - UPM_OK
    
    - [in] Télécharger a réussi. Le client définit cette information après le téléchargement d’informations sur le serveur.
    
  - UPM_MOVED
    
    - [in] L’élément a été déplacé avec succès.
    
  - UPM_COMMIT
    
    - [in] Valider l’état de chargement maintenant.
    
  - UPM_DELETE
    
    - [in] Supprimez l’élément maintenant.
    
  - UPM_SAVE
    
    - [in] Enregistrez les modifications apportées à l’élément.
    
_pmsg_
  
> [out] Ouvrir l’objet d’élément. Voir mapidefs.h pour la définition de type **de LPMESSAGE**. 
    
_meid_
  
> [out] ID d’entrée de l’élément.
    
_binReserved1_
  
> [in] Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge. 
    
_binReserved2_
  
> [in] Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge. 
    
_feid_
  
> [out] ID d’entrée du dossier source, si l’élément a été déplacé.
    
_binChg_
  
> [out] Modifier la clé de l’élément de destination, si l’élément a été déplacé. Voir mapidefs.h pour la définition de type **de SBinary**. 
    
_binPcl_
  
> [out] Modifier la liste de l’élément de destination, si l’élément a été déplacé. Voir mapidefs.h pour la définition de type **de SBinary**. 
    
_skeySrc_
  
> [out] Clé source de l’élément source, si l’élément a été déplacé.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

