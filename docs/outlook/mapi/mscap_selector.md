---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338674"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
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
  
> Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge. 
    
 *MSCAP_SEL_FOLDER* 
  
> Fonctionnalités de prise en charge des dossiers sur une banque.
    
 *MSCAP_SEL_RESERVED3* 
  
> Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Fonctionnalités de prise en charge des restrictions sur une banque.
    

