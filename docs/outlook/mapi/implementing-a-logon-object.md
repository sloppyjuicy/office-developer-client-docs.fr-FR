---
title: Implémentation d’un objet d’ouverture de session
description: Chaque carnet d’adresses, magasin de messages et fournisseur de transport instancie un objet d’ouverture de session dans le cadre de son implémentation d’IABProvider, IMSProvider ou IXPProvider.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
ms.openlocfilehash: 5718d01d14f2cb02d81d6219e741eb1ad63006ab
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828445"
---
# <a name="implementing-a-logon-object"></a>Implémentation d’un objet d’ouverture de session

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque carnet d’adresses, magasin de messages et fournisseur de transport instancie un objet d’ouverture de session dans le cadre de son implémentation [d’IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md) ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Les objets d’ouverture de session implémentent des méthodes qui aident les demandes des clients du service MAPI. Selon votre type de fournisseur de services, votre objet d’ouverture de session prend en charge l’une des interfaces suivantes. 
  
|**Interface de l’objet d’ouverture de session**|**Fournisseur**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Fournisseur de carnet d’adresses  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Fournisseur de magasin de messages  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Fournisseur de transport  <br/> |
   
Les fournisseurs de carnets d’adresses et de magasins de messages implémentent les fonctionnalités suivantes dans leurs objets d’ouverture de session :
  
- Prise en charge de la notification d’événements (méthodes **De conseil** et **Non-surveillance** ). Pour obtenir une vue d’ensemble de la notification d’événement, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur la prise en charge de la notification dans votre objet d’ouverture de session, consultez [Notification d’événement de prise en charge](supporting-event-notification.md). 
    
- Comparaison des identificateurs d’entrée (méthode **CompareEntryIDs** ). Pour obtenir des informations générales sur les identificateurs d’entrée, consultez [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md). Pour plus d’informations sur la comparaison des identificateurs d’entrée dans la méthode **CompareEntryIDs** de votre objet d’ouverture de session, consultez [Prise en charge de l’accès aux objets et de la comparaison](supporting-object-access-and-comparison.md).
    
- Accès à des informations d’erreur supplémentaires (méthode **GetLastError** ). Pour plus d’informations sur la gestion des erreurs dans MAPI, consultez [Gestion des erreurs dans MAPI](error-handling-in-mapi.md). 
    
- Accès aux objets implémentés par le fournisseur de services (méthode **OpenEntry** ). Pour plus d’informations, consultez [Prise en charge de l’accès aux objets et de la comparaison](supporting-object-access-and-comparison.md).
    
- Accès à un objet status (méthode **OpenStatusEntry** ). Pour obtenir des informations générales sur les objets d’état, consultez [Objets d’état MAPI](mapi-status-objects.md). Pour plus d’informations sur l’implémentation d’un objet d’état, consultez [l’implémentation de l’objet d’état](status-object-implementation.md).
    
- Processus de fermeture de session (méthode **Logoff** ). Pour plus d’informations, consultez [Arrêter un fournisseur de services](shutting-down-a-service-provider.md).
    
Si votre fournisseur est un fournisseur de carnet d’adresses, vous allez également implémenter les méthodes et fonctionnalités associées suivantes :
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) pour fournir une liste des modèles que vous prenez en charge pour la création de nouveaux destinataires. Pour plus d’informations, consultez [tables uniques](one-off-tables.md) ou [implémentation d’une table One-Off fournisseur](implementing-a-provider-one-off-table.md).
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) pour fournir l’accès à l’implémentation d’un destinataire dont les données résident dans un fournisseur de carnet d’adresses hôte. Pour plus d’informations, consultez [Agir en tant que fournisseur de carnets d’adresses étrangers](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::P repareRecips](iablogon-preparerecips.md) pour s’assurer que les propriétés appropriées sont disponibles pour tous les destinataires d’une liste de destinataires. Pour plus d’informations, consultez [IABLogon::P repareRecips](iablogon-preparerecips.md). 
    
L’objet d’ouverture de session d’un fournisseur de transport, qui implémente [IXPLogon : IUnknown](ixplogoniunknown.md), est très différent des objets d’ouverture de session implémentés par les autres types de fournisseurs de services. Il n’a que deux fonctionnalités en commun avec les autres objets d’ouverture de session : l’accès à un objet d’état via la méthode [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) et une opération de fermeture de session via la méthode [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) . Les fournisseurs de transport implémentent les fonctionnalités uniques suivantes dans leurs objets d’ouverture de session : 
  
- Inscription pour les types d’adresses ([méthode IXPLogon::AddressTypes](ixplogon-addresstypes.md) ). Pour plus d’informations sur l’inscription d’un type d’adresse, consultez [le fournisseur de transport et le modèle opérationnel du spouleur MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Contrôle de la transmission de messages (méthodes [IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md) et [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) ). Pour plus d’informations, consultez [le modèle de réception de message](message-reception-model.md), [l’interaction avec le spouleur MAPI et le](interacting-with-the-mapi-spooler.md) [modèle de soumission de messages](message-submission-model.md).
    
- Validation d’état interne ([méthode IXPLogon::ValidateState](ixplogon-validatestate.md) ). 
    
- Possibilité de télécharger ou de charger des messages à la demande ([méthode IXPLogon::FlushQueues](ixplogon-flushqueues.md) ). Pour plus d’informations, consultez [Implémentation de la méthode FlushQueues](implementing-the-flushqueues-method.md).
    
- Possibilité d’interroger les messages en attente ([méthode IXPLogon::P oll](ixplogon-poll.md) ). Pour plus d’informations, consultez [Le modèle de réception de](message-reception-model.md) message.
    
- Détection de l’état d’inactivité ([IXPLogon::Idle](ixplogon-idle.md) , méthode). 
    
- Interaction avec le spouleur MAPI ([méthode IXPLogon::TransportNotify](ixplogon-transportnotify.md) ). 
    
## <a name="see-also"></a>Voir aussi



[Implémentation de l’ouverture de session du fournisseur de services](implementing-service-provider-logon.md)

