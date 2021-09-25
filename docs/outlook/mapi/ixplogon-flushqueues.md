---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7fde61429307c2adf209b87b325deef69f098c35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584212"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande au fournisseur de transport de remettre immédiatement tous les messages entrants ou sortants en attente.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
 _cbTargetTransport_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpTargetTransport_
  
> [in] Réservé ; doit être NULL.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le purgement de file d’attente de messages est effectué. Les indicateurs suivants peuvent être définies :
    
FLUSH_DOWNLOAD 
  
> La ou les files d’attente de messages entrants doivent être vidées.
    
FLUSH_FORCE 
  
> Le fournisseur de transport doit traiter cette demande, si possible, même si cela prend beaucoup de temps. 
    
FLUSH_NO_UI 
  
> Le fournisseur de transport ne doit pas afficher d’interface utilisateur.
    
FLUSH_UPLOAD 
  
> La ou les files d’attente de messages sortants doivent être vidées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPLogon::FlushQueues** pour informer le fournisseur de transport que lepooler MAPI est sur le point de commencer le traitement des messages. Le fournisseur de transport doit appeler la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour définir un bit approprié pour son état dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sa ligne d’état. Après avoir mis à jour sa ligne d’état, le fournisseur de transport doit S_OK pour **l’appel FlushQueues.** Lepooler MAPI commence ensuite à envoyer des messages, l’opération étant synchrone avec lepooler MAPI. 
  
Pour prendre en charge son implémentation de la méthode [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md) lepooler MAPI appelle **IXPLogon::FlushQueues** pour tous les objets d’ouverture de session pour les fournisseurs de transport actifs qui s’exécutent dans une session de profil. Lorsque la méthode **FlushQueues** d’un fournisseur de transport est appelée à la suite d’un appel d’application cliente à **IMAPIStatus::FlushQueues**, le traitement des messages se produit de manière asynchrone pour le client.
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

