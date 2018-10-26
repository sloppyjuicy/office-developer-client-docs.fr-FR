---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1c66032788758b04558a37a4c35ff4dd6c702fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568265"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’intention de poursuivre du client MAPI arrêté.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le sous-système MAPI a tenté d’informer les fournisseurs MAPI chargés que le client MAPI sur le point d’effectuer un arrêt rapide.
    
## <a name="remarks"></a>Remarques

Pour éviter toute perte de données à partir de l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes **IMAPIClientShutdown::NotifyProcessShutdown** et [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) en fonction du résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Pour plus d’informations, voir [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

