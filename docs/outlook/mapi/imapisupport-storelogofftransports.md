---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421381"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande le lancement ordonné d'une banque de messages.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in, out] Masque de des indicateurs qui contrôle la manière dont la déconnexion du magasin de messages se produit. Lors de l'entrée, tous les indicateurs de ce paramètre s'excluent mutuellement; un seul des indicateurs suivants peut être défini par appel:
    
LOGOFF_ABORT 
  
> Toute activité de fournisseur de transport pour cette banque doit être arrêtée avant la fermeture de session. Le contrôle est renvoyé au client après l'arrêt de l'activité et le spouleur MAPI s'est déconnecté de la Banque. Si une activité de transport a lieu, la déconnexion n'a pas lieu et aucune modification n'est apportée au comportement du spouleur MAPI ou du fournisseur de transport. S'il n'y a actuellement aucune activité, le spouleur MAPI libère la Banque. 
    
LOGOFF_NO_WAIT 
  
> Le spouleur MAPI doit libérer le magasin et renvoyer le contrôle au client immédiatement après l'envoi de tous les messages sortants prêts à être envoyés. Si la Banque de messages est dotée de la boîte de réception par défaut, tout message en cours de traitement est reçu, puis la réception supplémentaire est désactivée. 
    
LOGOFF_ORDERLY 
  
> Le spouleur MAPI doit libérer le magasin et renvoyer le contrôle au client immédiatement après la fin du traitement des messages en attente. Aucun nouveau message ne doit être traité. 
    
LOGOFF_PURGE 
  
> Fonctionne de la même manière que l'indicateur LOGOFF_NO_WAIT. L'indicateur LOGOFF_PURGE renvoie le contrôle à l'appelant une fois l'opération terminée. 
    
LOGOFF_QUIET 
  
> La déconnexion ne doit pas se produire si l'activité d'un fournisseur de transport a lieu. Le type d'activité qui a lieu est renvoyé sous la forme d'un indicateur sur la sortie.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> La déconnexion peut être terminée. Toutes les ressources associées à la Banque ont été libérées, et l'objet a été invalidé. Le spouleur MAPI a effectué ou exécutera toutes les demandes. Seule la méthode **IUnknown:: Release** de la Banque de messages doit être appelée à ce stade. 
    
LOGOFF_INBOUND 
  
> Un message arrive actuellement dans le magasin à partir d'un ou plusieurs fournisseurs de transport. 
    
LOGOFF_OUTBOUND 
  
> Un message est actuellement envoyé à partir de la Banque par un ou plusieurs fournisseurs de transport. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Il y a actuellement des messages dans la file d'attente des messages sortants pour le magasin.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La procédure de fermeture de session a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: StoreLogoffTransports** est implémentée pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages appellent **StoreLogoffTransports** pour donner aux applications clientes un contrôle sur la façon dont MAPI gère l'activité du fournisseur de transport lorsqu'une banque de messages se ferme. 
  
Si le magasin doit être déconnecté pour un autre processus, MAPI ignore un appel vers **StoreLogoffTransports** et renvoie l'indicateur LOGOFF_COMPLETE dans le paramètre _lpulFlags_ . 
  
Le comportement du fournisseur de banque suivant le retour de **StoreLogoffTransports** doit être basé sur la valeur de _lpulFlags_, qui indique l'état du système et transmet les instructions du client pour le comportement de fermeture de session. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **StoreLogoffTransports** est généralement appelé à partir de la méthode [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) d'un fournisseur de magasins. Toutefois, elle peut également être appelée à partir de la méthode **IUnknown:: Release** de la Banque de messages. Implémentez la méthode **Release** de votre banque de messages pour vérifier si un appel à **StoreLogoffTransports** s'est produit. Si un appel n'a pas été effectué, appelez **StoreLogoffTransports** avec l'indicateur LOGOFF_ABORT défini. 
  
Le paramètre _lpulFlags_ est défini sur un indicateur qui indique la façon dont le client nécessite l'arrêt de la Banque de messages. Déterminez le paramètre approprié pour _ulFlags_ en fonction de la valeur du paramètre correspondant dans l'appel à **StoreLogoff**. Autrement dit, si un client a appelé votre méthode **StoreLogoff** avec _ULFLAGS_ défini sur LOGOFF_ORDERLY, vous devez appeler **STORELOGOFFTRANSPORTS** avec _ulFlags_ défini sur LOGOFF_ORDERLY. 
  
Pour plus d'informations sur le processus de fermeture de la Banque de messages, consultez la rubrique [arrêt d'un fournisseur de banque de messages](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

