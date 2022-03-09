---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
ms.openlocfilehash: c28020e7de039dcd842af803b8b8e490e6a0558b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371057"
---
# <a name="skey"></a>SKEY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Clé source d’un Outlook de données.
  
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

