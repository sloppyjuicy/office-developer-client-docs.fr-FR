---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431357"
---
# <a name="upfld"></a>UPFLD

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le téléchargement d'un dossier lors de l' [État du dossier de chargement](upload-folder-state.md).
  
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
  
>  [out]/[in] indicateurs pour déterminer les actions appropriées pour le uplaod. 
    
  - UPF_NEW
    
    - remarquer Le dossier est nouveau.
    
  - UPF_MOD_PARENT
    
    - remarquer Le dossier a été déplacé.
    
  - UPF_MOD_PROPS
    
    - remarquer Les propriétés du dossier ont été modifiées.
    
  - UPF_DEL
    
    - remarquer Le dossier a été supprimé.
    
  - UPF_OK
    
    - dans Le chargement a réussi. Le client le définit après avoir téléchargé les informations de dossier sur le serveur.
    
_pfld_
  
> remarquer Objet Folder ouvert à télécharger.
    
_feid_
  
> [sortant] ID d’entrée du dossier.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

