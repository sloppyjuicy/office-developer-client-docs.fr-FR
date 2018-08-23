---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5d6b1dfcd3866b0d0e7151e9d5399e1274810d14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568202"
---
# <a name="imapiofflinegetcurrentstate"></a>IMAPIOffline::GetCurrentState

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Obtient l’état en ligne ou hors connexion en cours d’un objet en mode hors connexion.
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a>Paramètres

 _pulState_
  
> [out] L’état de ligne ou hors connexion en cours d’un objet en mode hors connexion. Il doit être une de ces deux valeurs :
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)


[Constantes MAPI](mapi-constants.md)

