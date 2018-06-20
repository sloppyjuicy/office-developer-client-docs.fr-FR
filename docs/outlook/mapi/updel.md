---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787417"
---
# <a name="updel"></a>UPDEL

  
  
**S’applique à**: Outlook 
  
Informations pour les éléments qui ont été supprimés dans un magasin local. Ces informations sont utilisées pendant le [téléchargement supprimer l’état](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membres

 _pupde_
  
>  [out] Vecteur d’entrées [UPDELE](updele.md) . 
    
 _cEnt_
  
> [out] Nombre d’entrées dans *pupde* . 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)

