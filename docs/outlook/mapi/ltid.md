---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
ms.openlocfilehash: 6343c0c43eaf50d9bf6c46867ea62b141b64c0b2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379884"
---
# <a name="ltid"></a>LTID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
ID générique à long terme d’un objet dans une Outlook de données.
  
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

