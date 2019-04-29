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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418147"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Interroge le sous-système MAPI pour la prise en charge de l'arrêt rapide fourni par les fournisseurs MAPI chargés.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le sous-système MAPI prend en charge le client MAPI pour l'arrêt rapide.
    
MAPI_E_NO_SUPPORT
  
> Le fournisseur MAPI ne prend pas en charge le client MAPI pour l'arrêt rapide.
    
## <a name="remarks"></a>Remarques

Le fait que le sous-système MAPI prenne en charge le client MAPI pour l'arrêt rapide dépend du paramètre de Registre Windows de l'utilisateur ou du comportement par défaut du client MAPI pour l'arrêt rapide. Cela dépend également de la capacité des fournisseurs MAPI chargés à prendre en charge la mise à l'arrêt rapide. Pour plus d'informations, consultez la rubrique options de l' [utilisateur à arrêt rapide](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

