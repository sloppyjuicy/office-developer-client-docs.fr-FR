---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 88512a6e55bc550e717dae4fda0ca41fce09d221
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571821"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’intention du client MAPI de poursuivre l’arrêt.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le sous-système MAPI a tenté d’informer les fournisseurs MAPI chargés que le client MAPI va faire un arrêt rapide.
    
## <a name="remarks"></a>Remarques

Pour éviter la perte de données suite à l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes **IMAPIClientShutdown::NotifyProcessShutdown** et [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) basées sur le résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Pour plus d’informations, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

