---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtient une interface ISocialPerson basée sur le paramètre userID.
ms.openlocfilehash: 7546232b4ea758331dfd2ff5f794a0d14cafd590
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608817"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Obtient une interface [ISocialPerson](isocialpersoniunknown.md) basée sur le _paramètre userID._ 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Paramètres

_userId_
  
> [in] Chaîne qui contient un ID d’utilisateur ou une adresse SMTP d’une personne.
    
_result_
  
> [out] Interface **ISocialPerson.** 
    
## <a name="remarks"></a>Remarques

Le  _paramètre userID_ doit être un ID d’utilisateur ou une adresse SMTP. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

