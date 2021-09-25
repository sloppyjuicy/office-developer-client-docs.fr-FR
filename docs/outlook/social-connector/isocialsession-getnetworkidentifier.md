---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donnée.
ms.openlocfilehash: deaaf3e3380602738e9427d403db658c0f1f62df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560325"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donnée. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Paramètres

_networkIdentifier_
  
> [out] Chaîne qui contient un identificateur de réseau social unique.
    
## <a name="remarks"></a>Remarques

Un identificateur réseau unique est une chaîne qui identifie Outlook réseau social du fournisseur OSC (Social Connector). Cette méthode peut également renvoyer E_NOTIMPL.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

