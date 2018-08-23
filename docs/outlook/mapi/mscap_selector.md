---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588124"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

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
    

