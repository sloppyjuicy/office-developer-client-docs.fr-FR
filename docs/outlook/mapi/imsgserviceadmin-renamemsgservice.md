---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309981"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconseillé. Affecte un nouveau nom à un service de messagerie. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique pour le service de messagerie à renommer. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpszDisplayName_
  
> dans Pointeur vers le nouveau nom du service de messagerie.
    
## <a name="return-value"></a>Valeur renvoyée

MAPI_E_NO_SUPPORT 
  
> MAPI ne prend pas en charge le changement de nom de ce service de messagerie. **RenameMsgService** renvoie toujours cette valeur. 
    
## <a name="remarks"></a>Remarques

Pour attribuer un nouveau nom à un service de messagerie, les clients doivent utiliser la propriété **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) du service de messagerie. Les noms des fournisseurs de services dans un service de messagerie sont stockés dans leurs propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

