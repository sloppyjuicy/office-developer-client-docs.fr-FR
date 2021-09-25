---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifie un utilisateur qui peut ou non avoir des données de libre/occupé disponibles.
ms.openlocfilehash: e3c67d8cf4e858fa6b5bdde7bb1714c5caacb484
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568039"
---
# <a name="fbuser"></a>FBUser

Identifie un utilisateur qui peut ou non avoir des données de libre/occupé disponibles.
  
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
  
> Longueur de l’ID d’entrée de l’utilisateur de messagerie tel que représenté par l’interface [IMailUser.](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) 
    
_m_lpEid_
  
> ID d’entrée de l’utilisateur de messagerie tel que représenté par l’interface **IMailUser.** 
    
_m_ulReserved_
  
> Ce paramètre est réservé à un Outlook interne et n’est pas pris en charge.
    
_m_pwszReserved_
  
> Ce paramètre est réservé à un Outlook interne et n’est pas pris en charge.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API Disponibilité](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

