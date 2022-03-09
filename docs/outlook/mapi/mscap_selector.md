---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
ms.openlocfilehash: 04356840e0a7f45f3dc6f23f6dae7f4deec87ca6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371820"
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
    

