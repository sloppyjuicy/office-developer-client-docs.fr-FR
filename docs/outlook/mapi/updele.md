---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360542"
---
# <a name="updele"></a>UPDELE

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations étendues pour les éléments qui ont été supprimés dans un magasin local. Ces informations sont utilisées lors de l' [État de suppression de chargement](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
> [out]/[in] indicateurs pour déterminer le comportement approprié pendant le téléchargement.
    
  - UPD_ASSOC
    
    - remarquer L'élément est associé.
    
  - UPD_MOV
    
    - remarquer L'élément a été déplacé vers l'extérieur.
    
  - UPD_OK 
    
    - dans Le chargement a réussi. Le client le définit après avoir téléchargé des informations sur le serveur.
    
  - UPD_MOVED
    
    - dans L'élément a été déplacé.
    
  - UPD_UPDATE
    
    - dans Marquer l'élément source comme modifié.
    
  - UPD_COMMIT
    
    - dans Valider l'état de chargement maintenant (entrée 0).
    
_skey_
  
> remarquer Clé source de l'élément.
    
_dwReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
_binChg_
  
> remarquer Modifier la clé de l'élément de destination si l'élément a été déplacé.
    
_binPcl_
  
> remarquer Modifier la liste des éléments de destination si l'élément a été déplacé.
    
_skeyDst_
  
> remarquer Clé source de l'élément de destination si l'élément a été déplacé.
    
_pupmov_
  
> remarquer Informations sur le dossier de destination si l'élément a été déplacé.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

