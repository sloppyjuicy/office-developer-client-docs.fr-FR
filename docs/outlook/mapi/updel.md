---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
ms.openlocfilehash: 5cd049ff2c6f25e70712d0e988c47a2460a2be39
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380395"
---
# <a name="updel"></a>UPDEL

**S’applique à** : Outlook 2013 | Outlook 2016
  
Informations pour les éléments qui ont été supprimés dans un magasin local. Ces informations sont utilisées pendant l’état [de suppression de téléchargement](upload-delete-status-state.md).
  
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
  
> [out] Vecteur des [entrées UPDELE](updele.md) .

 _cEnt_
  
> [out] Nombre _d’entrées dans le nœud_.

## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
