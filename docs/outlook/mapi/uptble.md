---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329707"
---
# <a name="uptble"></a>UPTBLE

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations étendues pour le téléchargement du contenu d'un dossier lors de l'état de la [table de chargement](upload-table-state.md).
  
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
  
>  remarquer Index permettant de suivre le téléchargement du nombre _cEntMod_ d'éléments nouveaux ou modifiés. 
    
 _cEntMod_
  
>  remarquer Nombre d'éléments nouveaux ou modifiés dans le dossier. 
    
 _iEntRead_
  
>  remarquer Index permettant de suivre le téléchargement du nombre d'éléments de lecture _cEntRead_ . 
    
 _cEntRead_
  
>  remarquer Nombre d'éléments lus dans le dossier. 
    
 _iEntDel_
  
>  remarquer Index permettant de suivre le téléchargement du nombre d'éléments supprimés _cEntDel_ . 
    
 _cEntDel_
  
>  remarquer Nombre d'éléments supprimés dans le dossier. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

