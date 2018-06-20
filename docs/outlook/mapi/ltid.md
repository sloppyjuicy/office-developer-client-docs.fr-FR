---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784532"
---
# <a name="ltid"></a>LTID

  
  
**S’applique à**: Outlook 
  
Générique ID termes Long d’un objet dans un magasin d’Outlook.
  
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

 _GUID_
  
- [out] Le GUID du serveur qui a créé l’objet.
    
 _globcnt_
  
- [out] Numéro unique 6 octets qui identifie l’objet au sein de la banque d’Outlook.
    
 _wLevel_
  
- [out] Niveau de la hiérarchie de l’identificateur d’entrée pour un dossier Public favoris Exchange.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[FEID](feid.md)

