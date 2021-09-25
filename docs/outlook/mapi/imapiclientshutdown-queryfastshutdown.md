---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 487ef45b6ef611114d841f8f4c585a059d09265d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580012"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Interroge le sous-système MAPI pour obtenir la prise en charge de l’arrêt rapide fourni par les fournisseurs MAPI chargés.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le sous-système MAPI prend en charge le client MAPI pour un arrêt rapide.
    
MAPI_E_NO_SUPPORT
  
> Le fournisseur MAPI ne prend pas en charge le client MAPI pour un arrêt rapide.
    
## <a name="remarks"></a>Remarques

Le fait que le sous-système MAPI prend en charge le client MAPI pour l’arrêt rapide dépend du paramètre de Registre Windows de l’utilisateur ou du comportement par défaut du client MAPI pour l’arrêt rapide. Cela dépend également de la capacité des fournisseurs MAPI chargés à prendre en charge l’arrêt rapide. Pour plus d’informations, voir [Options utilisateur d’arrêt rapide.](fast-shutdown-user-options.md)
  
## <a name="see-also"></a>Voir aussi



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

