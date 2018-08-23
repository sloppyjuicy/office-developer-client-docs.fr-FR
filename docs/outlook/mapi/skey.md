---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 26b08535d81cb961ed0ace70ea227316b30cd526
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573459"
---
# <a name="skey"></a>SKEY

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Clé de la source d’un élément Outlook.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a>Members

 _GUID_
  
> GUID du serveur de création de l’objet.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[UPDELE](updele.md)
  
[UPMSG](upmsg.md)
  
[UPREADE](upreade.md)

