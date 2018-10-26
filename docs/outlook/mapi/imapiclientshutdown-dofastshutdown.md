---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 41c4ee65ce6ae8f2e0d978f1e2bd95adb4f5872a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575174"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’intention du client MAPI pour quitter le processus de client immédiatement.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le sous-système MAPI a indiqué pour les fournisseurs MAPI chargés que le client MAPI vient de quitter immédiatement, et les fournisseurs MAPI sont prêts pour la sortie du client.
    
MAPI_E_NO_SUPPORT
  
> Le sous-système MAPI ne gère pas l’arrêt rapide du client.
    
## <a name="remarks"></a>Remarques

Pour éviter toute perte de données à partir de l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et **IMAPIClientShutdown::DoFastShutdown** en fonction du résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Pour plus d’informations, voir [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

