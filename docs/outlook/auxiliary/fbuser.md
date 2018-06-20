---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifie un utilisateur qui peut ou non posséder des informations de disponibilité des données disponibles.
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782553"
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

## <a name="members"></a>Membres

_m_cbEid_
  
> La longueur de l’identificateur d’entrée de l’utilisateur de messagerie, tel que représenté par l’interface [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) . 
    
_m_lpEid_
  
> L’identificateur d’entrée de l’utilisateur de messagerie, tel que représenté par l’interface **IMailUser** . 
    
_m_ulReserved_
  
> Ce paramètre est réservé à un usage interne Outlook et n’est pas pris en charge.
    
_m_pwszReserved_
  
> Ce paramètre est réservé à un usage interne Outlook et n’est pas pris en charge.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de type disponible/occupé](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

