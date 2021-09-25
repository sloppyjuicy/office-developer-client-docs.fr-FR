---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: aeeed580fbe7048f8539fb561e3446ef5c6095bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566597"
---
# <a name="skey"></a>SKEY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Clé source d’un Outlook’élément.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a>Membres

 _guid_
  
> GUID du serveur qui crée l’objet.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[UPDELE](updele.md)
  
[UPMSG](upmsg.md)
  
[UPREADE](upreade.md)

