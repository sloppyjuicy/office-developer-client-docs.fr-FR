---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419435"
---
# <a name="ltid"></a>LTID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
ID générique à long terme d’un objet dans un magasin Outlook de données.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Membres

 _guid_
  
- [out] GUID du serveur qui a créé l’objet.
    
 _globcnt_
  
- [out] Nombre unique de 6 Outlook.
    
 _wLevel_
  
- [out] Niveau de hiérarchie de l’ID d’entrée d’Exchange dossier public favori.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[FEID](feid.md)

