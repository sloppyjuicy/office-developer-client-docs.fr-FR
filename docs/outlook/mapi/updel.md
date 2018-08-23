---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581124"
---
# <a name="updel"></a>UPDEL

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Informations pour les éléments qui ont été supprimés dans un magasin local. Ces informations sont utilisées pendant le [téléchargement supprimer l’état](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupde_
  
>  [out] Vecteur d’entrées [UPDELE](updele.md) . 
    
 _cEnt_
  
> [out] Nombre d’entrées dans *pupde* . 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)

