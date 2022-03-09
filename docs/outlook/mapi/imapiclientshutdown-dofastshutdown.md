---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
ms.openlocfilehash: 35117c318149df090dd12a1d82169d8b41711c22
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377511"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’intention du client MAPI de quitter immédiatement le processus client.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le sous-système MAPI a indiqué aux fournisseurs MAPI chargés que le client MAPI se quitte immédiatement et que les fournisseurs MAPI sont prêts pour la sortie du client.
    
MAPI_E_NO_SUPPORT
  
> Le sous-système MAPI ne prend pas en charge l’arrêt rapide du client.
    
## <a name="remarks"></a>Remarques

Pour éviter la perte de données suite à l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et **IMAPIClientShutdown::D oFastShutdown** en fonction du résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Pour plus d’informations, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

