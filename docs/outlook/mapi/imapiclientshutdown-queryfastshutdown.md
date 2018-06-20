---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 059d0d4427a8f2d68795a671d77fb9e3d84294f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783709"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**S’applique à**: Outlook 
  
Requêtes du sous-système MAPI pour arrêt rapide prennent en charge fournie par les fournisseurs MAPI chargés.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> Le sous-système MAPI prend en charge le client MAPI pour rapide de l’arrêt.
    
MAPI_E_NO_SUPPORT
  
> Le fournisseur MAPI ne gère pas le client MAPI pour rapide de l’arrêt.
    
## <a name="remarks"></a>Remarques

Si le sous-système MAPI prend en charge le client MAPI à rapide d’arrêt dépend du paramètre de Registre Windows de l’utilisateur ou le comportement par défaut du client MAPI pour l’arrêt rapide. Cela dépend également la possibilité des fournisseurs MAPI chargés pour prendre en charge l’arrêt rapide. Pour plus d’informations, voir [Options d’utilisateur de l’arrêt rapide](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

