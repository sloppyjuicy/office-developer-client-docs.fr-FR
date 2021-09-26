---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
ms.openlocfilehash: 7b5f3c6d791fc543e892289964fb7ffdab5357e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620855"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports
 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande la publication ordonnée d’une boutique de messages.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in, out] Masque de bits d’indicateurs qui contrôle la façon dont la ouverture de logo de la boutique de messages se produit. Lors de l’entrée, tous les indicateurs de ce paramètre s’excluent mutuellement ; Un seul des indicateurs suivants peut être définie par appel :
    
LOGOFF_ABORT 
  
> Toute activité de fournisseur de transport pour ce magasin doit être arrêtée avant la ff. Le contrôle est renvoyé au client une fois l’activité arrêtée et lepooler MAPI a ouvert une session hors du magasin. Si une activité de transport a lieu, la logoff ne se produit pas et le comportement du fournisseur de transport ou dupooler MAPI ne change pas. S’il n’y a actuellement aucune activité, lepooler MAPI libère le magasin. 
    
LOGOFF_NO_WAIT 
  
> Lepooler MAPI doit libérer le magasin et retourner le contrôle au client immédiatement après l’envoi de tous les messages sortants prêts à être envoyés. Si la boîte de réception par défaut de la boutique de messages est présente, tout message in-process est reçu, puis la réception est désactivée. 
    
LOGOFF_ORDERLY 
  
> Lepooler MAPI doit libérer la boutique et retourner le contrôle au client immédiatement après la fin du traitement des messages en attente. Aucun nouveau message ne doit être traitée. 
    
LOGOFF_PURGE 
  
> Fonctionne de la même manière que l’indicateur LOGOFF_NO_WAIT’un autre. L’LOGOFF_PURGE de contrôle renvoie le contrôle à l’appelant une fois l’exécution terminée. 
    
LOGOFF_QUIET 
  
> La logoff ne doit pas se produire si une activité de fournisseur de transport a lieu. Le type d’activité en cours est renvoyé sous forme d’indicateur sur la sortie.

Lors de la sortie, lepooler MAPI peut renvoyer un ou plusieurs des indicateurs suivants :
    
LOGOFF_COMPLETE 
  
> La ff de logo peut se terminer. Toutes les ressources associées au magasin ont été libérées et l’objet a été invalidé. Lepooler MAPI a effectué ou effectuera toutes les demandes. Seule la méthode **IUnknown::Release** de la boutique de messages doit être appelée à ce stade. 
    
LOGOFF_INBOUND 
  
> Un message est actuellement envoyé dans la boutique par un ou plusieurs fournisseurs de transport. 
    
LOGOFF_OUTBOUND 
  
> Un message est actuellement envoyé à partir de la boutique par un ou plusieurs fournisseurs de transport. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Il existe actuellement des messages dans la file d’attente sortante pour la boutique.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La procédure de création d’une logoff a réussi.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::StoreLogoffTransports** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages appellent **StoreLogoffTransports** pour donner aux applications clientes un certain contrôle sur la façon dont MAPI gère l’activité des fournisseurs de transport lors de la fermeture d’une magasin de messages. 
  
Si un autre processus a le magasin à ouvrir pour le même profil, MAPI ignore un appel à **StoreLogoffTransports** et renvoie l’indicateur LOGOFF_COMPLETE dans le paramètre _lpulFlags._ 
  
Le comportement du fournisseur de magasin suivant le retour de **StoreLogoffTransports** doit être basé sur la valeur de  _lpulFlags_, qui indique l’état du système et transmet les instructions client pour le comportement de la logoff. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **StoreLogoffTransports est** généralement appelé à partir de la méthode [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) d’un fournisseur de magasins. Toutefois, elle peut également être appelée à partir de la **méthode IUnknown::Release** de la boutique de messages. **Implémentez la** méthode Release de votre magasin de messages pour vérifier si un appel à **StoreLogoffTransports** s’est produit. Si un appel ne s’est pas produit, appelez **StoreLogoffTransports** avec l’indicateur LOGOFF_ABORT de données. 
  
Le  _paramètre lpulFlags_ est paramétré sur un indicateur qui indique comment le client requiert l’arrêt de la magasin de messages. Déterminez le paramètre approprié pour  _ulFlags_ en fonction du paramètre correspondant dans l’appel **à StoreLogoff**. Autrement dit, si un client a appelé votre méthode **StoreLogoff** avec  _ulFlags_ définie sur LOGOFF_ORDERLY, vous devez appeler **StoreLogoffTransports** avec  _ulFlags_ définie sur LOGOFF_ORDERLY. 
  
Pour plus d’informations sur le processus de fermeture de la boutique de messages, voir [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

