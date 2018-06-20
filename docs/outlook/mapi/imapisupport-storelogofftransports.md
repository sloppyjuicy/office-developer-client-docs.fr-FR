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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6624c4abf05dc7df9fc79df43f1d0fe76251d052
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784062"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**S’applique à**: Outlook 
  
Demande la version ordonnée d’une banque de messages.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [entrée, sortie] Masque de bits d’indicateurs qui contrôle la déconnexion de la banque message se produit. À l’entrée, tous les indicateurs pour ce paramètre sont mutuellement ; seul un des indicateurs suivants peut être défini par l’appel :
    
LOGOFF_ABORT 
  
> Toute activité du fournisseur de transport pour ce magasin doit être arrêtée avant la fermeture de session. Contrôle est retourné au client une fois que l’activité est arrêtée et le spouleur MAPI est déconnecté de la banque. Si aucune activité de transport a lieu, la fermeture de session ne se produit pas et aucune modification dans le comportement du fournisseur MAPI spouleur ou de transport a lieu. S’il n’existe actuellement aucune activité, le spouleur MAPI libère le magasin. 
    
LOGOFF_NO_WAIT 
  
> Le spouleur MAPI doit libérer le magasin et retourner le contrôle au client immédiatement les messages sortants après tout qui est prêt à être envoyé. Si la banque de messages est la boîte de réception par défaut, tout message en cours est reçu, puis réception supplémentaire est désactivée. 
    
LOGOFF_ORDERLY 
  
> Le spouleur MAPI doit libérer le magasin et retourner le contrôle au client dès l’appel en attente de messages sont terminées de traitement. Aucuns nouveaux messages ne doivent être traités. 
    
LOGOFF_PURGE 
  
> Fonctionnement de la même que l’indicateur LOGOFF_NO_WAIT. L’indicateur LOGOFF_PURGE retourne le contrôle à l’appelant après la fin. 
    
LOGOFF_QUIET 
  
> La fermeture de session ne doit pas se produire si une activité de fournisseur de transport a lieu. Le type d’activité en cours est renvoyé comme un indicateur de sortie.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> Procéder à la fermeture de session. Toutes les ressources associées au magasin ont été publiées, et l’objet a été désactivé. Le spouleur MAPI a effectué ou effectuera toutes les demandes. Uniquement les méthode **IUnknown::Release** de la banque de messages doivent être appelée à ce stade. 
    
LOGOFF_INBOUND 
  
> Un message est actuellement provenant dans le magasin d’un ou plusieurs fournisseurs de transport. 
    
LOGOFF_OUTBOUND 
  
> Un message est actuellement en cours envoyé à partir de la banque par un ou plusieurs fournisseurs de transport. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Il existe actuellement des messages dans la file d’attente sortante pour le magasin.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La procédure de fermeture de session a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::StoreLogoffTransports** est implémentée pour les objets de prise en charge de fournisseur de magasin de message. Fournisseurs de magasins message appellent **StoreLogoffTransports** pour fournir des applications clientes contrôler la fermeture d’activité de fournisseur de transport de handles MAPI comme une banque de messages. 
  
Si un autre processus a le magasin de session ouvrir pour le même profil, MAPI ignore un appel à **StoreLogoffTransports** et retourne l’indicateur LOGOFF_COMPLETE dans le paramètre _lpulFlags_ . 
  
Le comportement du fournisseur de banque après le retour de **StoreLogoffTransports** doit être basé sur la valeur de _lpulFlags_, qui indique l’état du système et des instructions pour le comportement de fermeture de session client dans le cas contraire. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **StoreLogoffTransports** est généralement appelée à partir [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) méthode d’un fournisseur de magasins. Toutefois, il peut également être appelée à partir de la méthode **IUnknown::Release** de la banque de messages. Implémentez la méthode de **publication** de vos messages afin de pouvoir vérifier si un appel à **StoreLogoffTransports** s’est produite. Si un appel n’a pas eu lieu, appelez **StoreLogoffTransports** avec l’indicateur LOGOFF_ABORT. 
  
Le paramètre _lpulFlags_ est défini à un indicateur qui indique comment le client requiert la banque de messages à arrêter. Déterminez le paramètre approprié pour _ulFlags_ en fonction de la valeur du paramètre dans l’appel de **StoreLogoff**correspondant. Autrement dit, si un client appelé votre méthode **StoreLogoff** avec _ulFlags_ défini sur LOGOFF_ORDERLY, vous devez appeler **StoreLogoffTransports** avec _ulFlags_ défini sur LOGOFF_ORDERLY. 
  
Pour plus d’informations sur le processus de fermeture de session de magasin de messages, voir [Arrêt vers le bas un Message Store Provider](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

