---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 43b7f65987948b600420ee288dd8b7e0bcea5325
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609242"
---
# <a name="updele"></a>UPDELE

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations étendues pour les éléments qui ont été supprimés dans un magasin local. Ces informations sont utilisées pendant [l’état de suppression de téléchargement.](upload-delete-status-state.md)
  
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
  
> [out]/[in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.
    
  - UPD_ASSOC
    
    - [out] L’élément est associé.
    
  - UPD_MOV
    
    - [out] L’élément a été déplacé vers l’avant.
    
  - UPD_OK 
    
    - [in] Télécharger a réussi. Le client définit cette information après le téléchargement d’informations sur le serveur.
    
  - UPD_MOVED
    
    - [in] L’élément a été déplacé avec succès.
    
  - UPD_UPDATE
    
    - [in] Marquez l’élément source comme modifié.
    
  - UPD_COMMIT
    
    - [in] Valider l’état de chargement maintenant (entrée 0).
    
_skey_
  
> [out] Clé source de l’élément.
    
_dwReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
_binChg_
  
> [out] Modifier la clé de l’élément de destination si l’élément a été déplacé.
    
_binPcl_
  
> [out] Modifier la liste de l’élément de destination si l’élément a été déplacé.
    
_skeyDst_
  
> [out] Clé source de l’élément de destination si l’élément a été déplacé.
    
_mov_
  
> [out] Informations sur le dossier de destination si l’élément a été déplacé.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

