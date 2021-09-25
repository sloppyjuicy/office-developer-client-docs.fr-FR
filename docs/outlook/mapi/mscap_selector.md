---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ab0041d579f4c8aac6d531fe94a4b18ba7825379
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575385"
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
  
> Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_FOLDER* 
  
> Fonctionnalités de prise en charge des dossiers dans une boutique.
    
 *MSCAP_SEL_RESERVED3* 
  
> Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Fonctionnalités relatives à la prise en charge des restrictions sur un magasin.
    

