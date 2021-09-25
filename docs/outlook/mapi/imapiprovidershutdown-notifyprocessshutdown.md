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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 25ea48649d1a58fbc753024e048e15d068374e90
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575862"
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

