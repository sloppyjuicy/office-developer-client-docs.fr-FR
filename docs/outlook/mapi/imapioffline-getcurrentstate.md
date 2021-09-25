---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 29fa50c92899ce0857a5a2934393c47b870e69ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567591"
---
# <a name="imapiofflinegetcurrentstate"></a>IMAPIOffline::GetCurrentState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient l’état actuel en ligne ou hors connexion d’un objet hors connexion.
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a>Paramètres

 _l’état de l’état de_
  
> [out] État actuel en ligne ou hors connexion d’un objet hors connexion. Elle doit être l’une des deux valeurs ci-après :
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)


[Constantes MAPI](mapi-constants.md)

