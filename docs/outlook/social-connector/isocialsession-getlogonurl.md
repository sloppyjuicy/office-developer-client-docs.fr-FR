---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtient une chaîne qui représente une URL qui est utilisée pour présenter un formulaire basé sur un navigateur à l’utilisateur lors de l’authentification web.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787605"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Obtient une chaîne qui représente une URL qui est utilisée pour présenter un formulaire basé sur un navigateur à l’utilisateur lors de l’authentification web.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Paramètres

_URL_
  
> [out] Chaîne qui contient une URL pour le formulaire utilisé dans l’authentification web.
    
## <a name="remarks"></a>Remarques

Une fois que le formulaire est présenté à l’utilisateur, la méthode [ISocialSession::LogonWeb](isocialsession-logonweb.md) est appelée avec une chaîne vide pour le paramètre _connectIn_ . 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

