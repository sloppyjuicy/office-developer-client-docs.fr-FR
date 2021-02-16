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
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413839"
---
# <a name="uptble"></a>UPTBLE

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations étendues pour le chargement du contenu d’un dossier pendant [l’état de la table de téléchargement.](upload-table-state.md)
  
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
  
>  [out] Index pour suivre le téléchargement du  _nombre cEntMod_ d’éléments nouveaux ou modifiés. 
    
 _cEntMod_
  
>  [out] Nombre d’éléments nouveaux ou modifiés dans le dossier. 
    
 _iEntRead_
  
>  [out] Index pour suivre le téléchargement du nombre d’éléments de lecture _cEntRead._ 
    
 _cEntRead_
  
>  [out] Nombre d’éléments lus dans le dossier. 
    
 _iEntDel_
  
>  [out] Index pour suivre le téléchargement du nombre d’éléments _supprimés par cEntDel._ 
    
 _cEntDel_
  
>  [out] Nombre d’éléments supprimés dans le dossier. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md) 
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

