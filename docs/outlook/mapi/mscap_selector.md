---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 420b2661e766ecf97a5e9e488e9c18f29cd91329
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19784891"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**S’applique à**: Outlook 
  
Spécifie les fonctionnalités à renvoyer pour une banque.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a>Membres

 *MSCAP_SEL_RESERVED1* 
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_FOLDER* 
  
> Fonctionnalités sur la prise en charge des dossiers dans une banque.
    
 *MSCAP_SEL_RESERVED3* 
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Prise en charge des restrictions sur un magasin de possibilités.
    

