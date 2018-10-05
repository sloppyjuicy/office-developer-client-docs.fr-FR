---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifie un utilisateur qui peut ou non posséder des informations de disponibilité des données disponibles.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387901"
---
# <a name="fbuser"></a>FBUser

Identifie un utilisateur qui peut ou non posséder des informations de disponibilité des données disponibles.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a>Members

_m_cbEid_
  
> La longueur de l’identificateur d’entrée de l’utilisateur de messagerie, tel que représenté par l’interface [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) . 
    
_m_lpEid_
  
> L’identificateur d’entrée de l’utilisateur de messagerie, tel que représenté par l’interface **IMailUser** . 
    
_m_ulReserved_
  
> Ce paramètre est réservé à un usage interne Outlook et n’est pas pris en charge.
    
_m_pwszReserved_
  
> Ce paramètre est réservé à un usage interne Outlook et n’est pas pris en charge.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API Disponibilité](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

