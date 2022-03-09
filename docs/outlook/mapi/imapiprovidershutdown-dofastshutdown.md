---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
ms.openlocfilehash: 7a139ed6b782814e21f4fa77a7914d542f48639b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382082"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique au fournisseur MAPI que le client MAPI quitte immédiatement, afin que le fournisseur MAPI continue à apporter des modifications afin d’éviter toute perte de données.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le fournisseur MAPI est prêt à quitter immédiatement le client MAPI. 
    
## <a name="see-also"></a>Voir aussi



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

