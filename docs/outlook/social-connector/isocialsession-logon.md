---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Ouvre une session sur le site de réseau social à l’aide du nom d’utilisateur et le mot de passe.
ms.openlocfilehash: d7a79767f3726f9748ea48839f1e190af2e9ec74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787613"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

Ouvre une session sur le site de réseau social à l’aide du nom d’utilisateur et le mot de passe.
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Paramètres

_nom d’utilisateur_
  
> [in] Chaîne qui contient le nom d’utilisateur à se connecter.
    
_mot de passe_
  
> [in] Chaîne qui contient le mot de passe pour vous connecter.
    
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

