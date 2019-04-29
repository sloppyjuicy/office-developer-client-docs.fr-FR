---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtient une valeur de type String qui représente une URL utilisée pour présenter un formulaire basé sur un navigateur à l'utilisateur lors de l'authentification Web.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427912"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Obtient une valeur de type String qui représente une URL utilisée pour présenter un formulaire basé sur un navigateur à l'utilisateur lors de l'authentification Web.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Paramètres

_url_
  
> remarquer Chaîne qui contient une URL pour le formulaire utilisé dans l'authentification Web.
    
## <a name="remarks"></a>Remarques

Une fois que le formulaire est présenté à l'utilisateur, la méthode [ISocialSession:: LogonWeb](isocialsession-logonweb.md) est appelée avec une chaîne vide pour le paramètre _Connect_ . 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

