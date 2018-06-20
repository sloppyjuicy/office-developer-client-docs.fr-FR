---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4dd60ffe305d27db2c9118e11cccf692652d0d27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787418"
---
# <a name="updele"></a>UPDELE

**S’applique à**: Outlook 
  
Étendue des informations pour les éléments qui ont été supprimés dans un magasin local. Ces informations sont utilisées pendant le [téléchargement supprimer l’état](upload-delete-status-state.md).
  
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
  
> [out] / [in] indicateurs pour déterminer le comportement approprié lors du téléchargement.
    
  - UPD_ASSOC
    
    - [out] Élément est associé.
    
  - UPD_MOV
    
    - [out] Élément a été déplacé.
    
  - UPD_OK 
    
    - [in] Téléchargement a réussi. Le client définit après le téléchargement des informations sur le serveur.
    
  - UPD_MOVED
    
    - [in] Élément a été déplacé avec succès.
    
  - UPD_UPDATE
    
    - [in] Élément source marque modifiée.
    
  - UPD_COMMIT
    
    - [in] Valider l’état du téléchargement maintenant (entrée 0).
    
_SKEY_
  
> [out] Clé de la source de l’élément.
    
_dwReserved_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
_binChg_
  
> [out] Modifier la clé de l’élément de destination si l’élément a été déplacé.
    
_binPcl_
  
> [out] Modifier la liste des éléments de destination si l’élément a été déplacé.
    
_skeyDst_
  
> [out] Clé de la source de l’élément de destination, si l’élément a été déplacée.
    
_pupmov_
  
> [out] Informations de dossier de destination si l’élément a été déplacées.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

