---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326389"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique au fournisseur MAPI qu'un client MAPI va effectuer un arrêt rapide, afin que le fournisseur puisse prendre des mesures pour empêcher toute perte de données.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le fournisseur MAPI prend des mesures pour empêcher la perte de données lors de l'arrêt du client MAPI.
    
## <a name="see-also"></a>Voir aussi



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

