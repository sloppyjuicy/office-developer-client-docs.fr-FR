---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282830"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande que le fournisseur de transport remet immédiatement tous les messages entrants ou sortants en attente.
  
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
  
> dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.
    
 _cbTargetTransport_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpTargetTransport_
  
> dans MSR doit être NULL.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le vidage de la file d'attente de messages. Les indicateurs suivants peuvent être définis:
    
FLUSH_DOWNLOAD 
  
> La file d'attente de messages entrants ou les files d'attente doivent être vidées.
    
FLUSH_FORCE 
  
> Le fournisseur de transport doit traiter cette demande, si possible, même si cela prend du temps. 
    
FLUSH_NO_UI 
  
> Le fournisseur de transport ne doit pas afficher une interface utilisateur.
    
FLUSH_UPLOAD 
  
> La file d'attente de messages sortants ou les files d'attente doivent être vidées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon:: FlushQueues** pour conseiller au fournisseur de transport que le spouleur MAPI est sur le le traitement des messages. Le fournisseur de transport doit appeler la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) pour définir un bit approprié pour son état dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sa ligne d'État. Après la mise à jour de sa ligne d'État, le fournisseur de transport doit retourner S_OK pour l'appel **FlushQueues** . Le spouleur MAPI commence alors à envoyer des messages, l'opération étant synchrone vers le spouleur MAPI. 
  
Pour prendre en charge son implémentation de la méthode [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) , le spouleur MAPI appelle **IXPLogon:: FlushQueues** pour tous les objets d'ouverture de session des fournisseurs de transport actifs en cours d'exécution dans une session de profil. Lorsque la méthode **FlushQueues** d'un fournisseur de transport est appelée suite à l'appel d'une application cliente à **IMAPIStatus:: FlushQueues**, le traitement du message a lieu de manière asynchrone au client.
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

