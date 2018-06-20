---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f25b3fb967f4ed93ac38487f21145f35413764da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787422"
---
# <a name="upfld"></a>UPFLD

**S’applique à**: Outlook 
  
Informations de téléchargement d’un dossier au cours de l' [état du dossier de téléchargement](upload-folder-state.md).
  
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
  
>  [out] / [in] indicateurs pour déterminer les actions appropriées pour l’uplaod. 
    
  - UPF_NEW
    
    - [out] Dossier est nouveau.
    
  - UPF_MOD_PARENT
    
    - [out] Dossier a été déplacé.
    
  - UPF_MOD_PROPS
    
    - [out] Les propriétés de dossier ont été modifiées.
    
  - UPF_DEL
    
    - [out] Dossier a été supprimé.
    
  - UPF_OK
    
    - [in] Téléchargement a réussi. Le client définit après le téléchargement des informations sur les dossiers sur le serveur.
    
_pfld_
  
> [out] L’objet d’ouvrir le dossier à télécharger.
    
_feid_
  
> [out] ID d’entrée du dossier.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

