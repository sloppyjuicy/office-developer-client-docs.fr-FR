---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtient une interface ISocialPerson basée sur le paramètre userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439820"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Obtient une interface [ISocialPerson](isocialpersoniunknown.md) basée sur le paramètre _userid_ . 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Paramètres

_Identifi_
  
> dans Chaîne qui contient un ID d'utilisateur ou une adresse SMTP d'une personne.
    
_result_
  
> remarquer Une interface **ISocialPerson** . 
    
## <a name="remarks"></a>Remarques

Le paramètre _userid_ doit être un ID d'utilisateur ou une adresse SMTP. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

