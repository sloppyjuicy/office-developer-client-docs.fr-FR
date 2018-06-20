---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donné.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787732"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Obtient une chaîne qui représente un identificateur de réseau social unique pour une connexion de réseau social donné. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Paramètres

_networkIdentifier_
  
> [out] Chaîne qui contient un identificateur unique de réseau social.
    
## <a name="remarks"></a>Remarques

Un identificateur de réseau unique est une chaîne qui identifie le réseau social du fournisseur Outlook Social Connector (OSC). Cette méthode peut aussi renvoyer E_NOTIMPL.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

