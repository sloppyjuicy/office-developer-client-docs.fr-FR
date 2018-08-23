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
ms.openlocfilehash: 34d6eb0653c3eb550bf03242a2c1b2acc3330a13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572290"
---
# <a name="upfld"></a>UPFLD

**S’applique à**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

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
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

