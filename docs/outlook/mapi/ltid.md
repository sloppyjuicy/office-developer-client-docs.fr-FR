---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ec1902d05c6b5a8403fce4d872129b11159fd7ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592164"
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

