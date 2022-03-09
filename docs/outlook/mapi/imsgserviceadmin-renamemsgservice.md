---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
ms.openlocfilehash: 49e471eecc87fe7e4e17ed194d46cdf8bd7bc1f2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369328"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconseillé. Attribue un nouveau nom à un service de message. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message à renommer. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpszDisplayName_
  
> [in] Pointeur vers le nouveau nom du service de message.
    
## <a name="return-value"></a>Valeur renvoyée

MAPI_E_NO_SUPPORT 
  
> MAPI ne prend pas en charge le changement de nom de ce service de message. **RenameMsgService** renvoie toujours cette valeur. 
    
## <a name="remarks"></a>Remarques

Pour attribuer un nouveau nom à un service de message, les clients doivent utiliser la propriété **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) du service de message. Les noms des fournisseurs de services dans un service de messagerie sont stockés dans leurs propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

