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
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417202"
---
# <a name="mscap_selector"></a>MSCAP_SELECTOR

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les fonctionnalités à renvoyer pour un magasin.
  
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
  
> Ce membre est réservé à l’utilisation interne d’Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Ce membre est réservé à l’utilisation interne d’Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_FOLDER* 
  
> Fonctionnalités de prise en charge des dossiers dans une boutique.
    
 *MSCAP_SEL_RESERVED3* 
  
> Ce membre est réservé à l’utilisation interne d’Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Fonctionnalités relatives à la prise en charge des restrictions sur un magasin.
    

