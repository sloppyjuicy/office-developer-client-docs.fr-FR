---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592338"
---
# <a name="uptble"></a>UPTBLE

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Informations de téléchargement du contenu d’un dossier pendant la [Télécharger l’état de la table](upload-table-state.md)d’étendues.
  
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

## <a name="members"></a>Members

 _iEntMod_
  
>  [out] Index pour effectuer le suivi de téléchargement le nombre de _cEntMod_ d’éléments nouveaux ou modifiés. 
    
 _cEntMod_
  
>  [out] Nombre d’éléments nouveaux ou modifiés dans le dossier. 
    
 _iEntRead_
  
>  [out] Pour effectuer le suivi de téléchargement le nombre de _cEntRead_ lire des éléments d’index. 
    
 _cEntRead_
  
>  [out] Nombre d’éléments lus dans le dossier. 
    
 _iEntDel_
  
>  [out] Index pour effectuer le suivi de téléchargement le nombre de _cEntDel_ les éléments supprimés. 
    
 _cEntDel_
  
>  [out] Nombre d’éléments supprimés dans le dossier. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

