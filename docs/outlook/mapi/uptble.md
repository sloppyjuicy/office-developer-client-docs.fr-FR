---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
ms.openlocfilehash: f0af1bcb75f9008e0fc95778af54f9c9abdda5a9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376048"
---
# <a name="uptble"></a>UPTBLE

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations étendues pour le chargement du contenu d’un dossier pendant [l’état de la table de chargement](upload-table-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>Membres

 _iEntMod_
  
> [out] Index pour suivre le téléchargement du  _nombre cEntMod_ d’éléments nouveaux ou modifiés. 
    
 _cEntMod_
  
> [out] Nombre d’éléments nouveaux ou modifiés dans le dossier. 
    
 _iEntRead_
  
> [out] Index pour suivre le téléchargement du nombre d’éléments  _de lecture cEntRead_ . 
    
 _cEntRead_
  
> [out] Nombre d’éléments lus dans le dossier. 
    
 _iEntDel_
  
> [out] Index pour suivre le téléchargement du nombre d’éléments  _supprimés par cEntDel_ . 
    
 _cEntDel_
  
> [out] Nombre d’éléments supprimés dans le dossier. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

