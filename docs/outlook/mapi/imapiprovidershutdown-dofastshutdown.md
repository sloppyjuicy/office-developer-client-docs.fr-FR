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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5fc5914f6af792bb59d8063e87ceb29ca0ccf8ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620939"
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

