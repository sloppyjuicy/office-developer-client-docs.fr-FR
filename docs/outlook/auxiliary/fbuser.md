---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifie un utilisateur qui peut ou non disposer de données libres/occupées.
ms.openlocfilehash: d50d912e18b874eff07fb942b077eafb7444db68
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083435"
---
# <a name="fbuser"></a>FBUser

Identifie un utilisateur qui peut ou non disposer de données libres/occupées.
  
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
  
> Longueur de l’ID d’entrée de l’utilisateur de messagerie représenté par l’interface [IMailUser](/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) . 
    
_m_lpEid_
  
> ID d’entrée de l’utilisateur de messagerie représenté par l’interface **IMailUser** . 
    
_m_ulReserved_
  
> Ce paramètre est réservé à Outlook’utilisation interne et n’est pas pris en charge.
    
_m_pwszReserved_
  
> Ce paramètre est réservé à Outlook’utilisation interne et n’est pas pris en charge.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API Disponibilité](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)
