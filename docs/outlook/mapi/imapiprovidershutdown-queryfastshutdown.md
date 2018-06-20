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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783947"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**S’applique à**: Outlook 
  
Requêtes le fournisseur MAPI pour arrêt rapide prennent en charge. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> Le fournisseur MAPI prend en charge le client MAPI pour rapide de l’arrêt.
    
MAPI_E_NO_SUPPORT
  
> Le fournisseur MAPI ne gère pas le client MAPI pour rapide de l’arrêt.
    
## <a name="remarks"></a>Remarques

Fournisseurs MAPI qui n’ont pas besoin pour prendre en charge l’arrêt rapide client doivent toujours implémenter l’interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) et que la méthode de **IMAPIProviderShutdown::QueryFastShutdown** renvoie MAPI_E_NO_SUPPORT. Pour Outlook en tant qu’un client MAPI, cela entraîne à attendre que toutes les références externes doit être publié avant de quitter Outlook. 
  
Dans le Registre Windows de l’utilisateur en fonction de paramètre d’arrêt rapide, ne pas l’implémentation de l’interface **IMAPIProviderShutdown** n’empêche pas nécessairement un arrêt rapide du client. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

