---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donnée.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433275"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donnée. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Parameters

_networkIdentifier_
  
> [out] Chaîne qui contient un identificateur de réseau social unique.
    
## <a name="remarks"></a>Remarques

Un identificateur réseau unique est une chaîne qui identifie Outlook réseau social du fournisseur OSC (Social Connector). Cette méthode peut également renvoyer E_NOTIMPL.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

