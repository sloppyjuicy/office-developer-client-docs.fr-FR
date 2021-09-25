---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Obtient une interface ISocialSession.
ms.openlocfilehash: b26d02622ee4debe1136c3840d20e93648c69d25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629136"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

Obtient une interface [ISocialSession.](isocialsessioniunknown.md) 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Paramètres

_session_
  
> [out] Une interface **ISocialSession**. 
    
## <a name="remarks"></a>Remarques

Le Outlook Social Connector (OSC) utilise l’interface **ISocialSession** pour se connecter au réseau social. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

