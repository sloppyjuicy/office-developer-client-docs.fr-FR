---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtient une chaîne qui représente une URL utilisée pour présenter un formulaire basé sur un navigateur à l’utilisateur pendant l’authentification web.
ms.openlocfilehash: eeb822c40541ffb46fb8ac3087aa7bef21601d04
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590393"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Obtient une chaîne qui représente une URL utilisée pour présenter un formulaire basé sur un navigateur à l’utilisateur pendant l’authentification web.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Paramètres

_url_
  
> [out] Chaîne qui contient une URL pour le formulaire utilisé dans l’authentification web.
    
## <a name="remarks"></a>Remarques

Une fois le formulaire présenté à l’utilisateur, la méthode [ISocialSession::LogonWeb](isocialsession-logonweb.md) est appelée avec une chaîne vide pour le _paramètre connectIn._ 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

