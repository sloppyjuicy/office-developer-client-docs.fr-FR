---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
ms.openlocfilehash: 6592ad62479cba668e77ab4a5d90477858213157
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373129"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Interroge le fournisseur MAPI pour obtenir une prise en charge de l’arrêt rapide. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le fournisseur MAPI prend en charge le client MAPI pour un arrêt rapide.
    
MAPI_E_NO_SUPPORT
  
> Le fournisseur MAPI ne prend pas en charge le client MAPI pour un arrêt rapide.
    
## <a name="remarks"></a>Remarques

Les fournisseurs MAPI qui n’ont pas besoin de prendre en charge l’arrêt rapide du client doivent toujours implémenter l’interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) et faire en retour la méthode **IMAPIProviderShutdown::QueryFastShutdown** MAPI_E_NO_SUPPORT. Pour Outlook client MAPI, cela entraîne Outlook attendre que toutes les références externes soient libérées avant de se quitter. 
  
Selon le paramètre de Registre Windows de l’utilisateur pour l’arrêt rapide, le fait de ne pas implémenter l’interface **IMAPIProviderShutdown** n’empêche pas nécessairement un arrêt rapide du client. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

