---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787190"
---
# <a name="skey"></a>SKEY

  
  
**S’applique à**: Outlook 
  
Clé de la source d’un élément Outlook.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a>Membres

 _GUID_
  
> GUID du serveur de création de l’objet.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[UPDELE](updele.md)
  
[UPMSG](upmsg.md)
  
[UPREADE](upreade.md)

