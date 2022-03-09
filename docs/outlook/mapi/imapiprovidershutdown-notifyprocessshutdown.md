---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
ms.openlocfilehash: 60988b484fcc39c367868f251a2650f175cd91e2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378652"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique au fournisseur MAPI qu’un client MAPI va faire un arrêt rapide, afin que le fournisseur puisse prendre des mesures pour empêcher la perte de données.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le fournisseur MAPI prend des mesures pour empêcher la perte de données lorsque le client MAPI s’arrête.
    
## <a name="see-also"></a>Voir aussi



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

