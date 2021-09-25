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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 531653f794b38fec68fac206963df04b55af20d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580026"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’intention du client MAPI de quitter immédiatement le processus client.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le sous-système MAPI a indiqué aux fournisseurs MAPI chargés que le client MAPI quitte immédiatement et que les fournisseurs MAPI sont prêts pour la sortie du client.
    
MAPI_E_NO_SUPPORT
  
> Le sous-système MAPI ne prend pas en charge l’arrêt rapide du client.
    
## <a name="remarks"></a>Remarques

Pour éviter la perte de données suite à l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et **IMAPIClientShutdown::D oFastShutdown** basées sur le résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Pour plus d’informations, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

