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
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569854"
---
# <a name="ltid"></a>LTID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

 _GUID_
  
- [out] Le GUID du serveur qui a créé l’objet.
    
 _globcnt_
  
- [out] Numéro unique 6 octets qui identifie l’objet au sein de la banque d’Outlook.
    
 _wLevel_
  
- [out] Niveau de la hiérarchie de l’identificateur d’entrée pour un dossier Public favoris Exchange.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[FEID](feid.md)

