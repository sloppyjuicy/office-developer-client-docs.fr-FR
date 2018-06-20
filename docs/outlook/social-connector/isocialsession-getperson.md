---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtient une interface ISocialPerson en fonction du paramètre userID.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787608"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Obtient une interface [ISocialPerson](isocialpersoniunknown.md) en fonction du paramètre _userID_ . 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Paramètres

_userId_
  
> [in] Chaîne qui contient une utilisateur ID ou une adresse SMTP d’une personne.
    
_résultat_
  
> [out] Une interface **ISocialPerson** . 
    
## <a name="remarks"></a>Remarques

Le paramètre _userID_ doit être une utilisateur ID ou une adresse SMTP. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

