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
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436798"
---
# <a name="updel"></a>UPDEL

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations sur les éléments qui ont été supprimés dans un magasin local. Ces informations sont utilisées pendant [l’état de suppression de téléchargement.](upload-delete-status-state.md)
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membres

 _édéde_
  
>  [out] Vecteur des [entrées UPDELE.](updele.md) 
    
 _cEnt_
  
> [out] Nombre d’entrées  *dans le nœud*  . 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)

