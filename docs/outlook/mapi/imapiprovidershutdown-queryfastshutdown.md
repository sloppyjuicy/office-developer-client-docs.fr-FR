---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338485"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Interroge le fournisseur MAPI pour la prise en charge de l'arrêt rapide. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le fournisseur MAPI prend en charge le client MAPI pour l'arrêt rapide.
    
MAPI_E_NO_SUPPORT
  
> Le fournisseur MAPI ne prend pas en charge le client MAPI pour l'arrêt rapide.
    
## <a name="remarks"></a>Remarques

Les fournisseurs MAPI qui n'ont pas besoin de prendre en charge l'arrêt rapide client doivent toujours implémenter l'interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) et faire en sorte que la méthode **IMAPIProviderShutdown:: QueryFastShutdown** renvoie MAPI_E_NO_SUPPORT. Dans le cas d'Outlook en tant que client MAPI, Outlook attend que toutes les références externes soient libérées avant de se fermer. 
  
En fonction du paramètre de Registre Windows de l'utilisateur pour l'arrêt rapide, l'implémentation de l'interface **IMAPIProviderShutdown** n'empêche pas nécessairement un arrêt rapide du client. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

