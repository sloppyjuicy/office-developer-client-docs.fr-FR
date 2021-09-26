---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: edac057e9f8cc76d189d95019eebb969bc9c9e79
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623956"
---
# <a name="upfld"></a>UPFLD

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le chargement d’un dossier pendant [l’état du dossier de chargement.](upload-folder-state.md)
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a>Membres

_ulFlags_
  
>  [out]/[in] Indicateurs pour déterminer les actions appropriées pour la mettre à jour. 
    
  - UPF_NEW
    
    - [out] Le dossier est nouveau.
    
  - UPF_MOD_PARENT
    
    - [out] Le dossier a été déplacé.
    
  - UPF_MOD_PROPS
    
    - [out] Les propriétés du dossier ont été modifiées.
    
  - UPF_DEL
    
    - [out] Le dossier a été supprimé.
    
  - UPF_OK
    
    - [in] Télécharger a réussi. Le client définit cette information après le chargement des informations de dossier sur le serveur.
    
_pfld_
  
> [out] Objet de dossier ouvert à télécharger.
    
_feid_
  
> [sortant] ID d’entrée du dossier.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

