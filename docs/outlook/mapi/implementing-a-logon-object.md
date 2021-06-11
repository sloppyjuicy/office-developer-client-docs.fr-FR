---
title: Implémentation d’un objet Logon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433044"
---
# <a name="implementing-a-logon-object"></a>Implémentation d’un objet Logon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque carnet d’adresses, magasin de messages et fournisseur de transport ins instantique un objet d’ouverture de messagerie dans le cadre de son implémentation de [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Les objets d' logon implémentent des méthodes qui aident les demandes clientes de service MAPI. Selon votre type de fournisseur de services, votre objet d’accès prendra en charge l’une des interfaces suivantes. 
  
|**Interface d’objet d' logon**|**Fournisseur de services**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Fournisseur de carnet d’adresses  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Fournisseur de magasin de messages  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Fournisseur de transport  <br/> |
   
Les fournisseurs de carnet d’adresses et de magasin de messages implémentent les fonctionnalités suivantes dans leurs objets d’ouverture de messagerie :
  
- Prise en charge de la notification **d’événement (méthodes Advise** et **Unadvise).** Pour une vue d’ensemble de la notification d’événement, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur la prise en charge des notifications dans votre objet d’accès, voir [Notification d’événement de prise en charge.](supporting-event-notification.md) 
    
- Comparaison des identificateurs **d’entrée (méthode CompareEntryIDs).** Pour obtenir des informations générales sur les identificateurs d’entrée, voir [Identificateurs d’entrée MAPI.](mapi-entry-identifiers.md) Pour plus d’informations sur la comparaison des identificateurs d’entrée dans la méthode **CompareEntryIDs** de votre objet d’inscription, voir [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).
    
- Accès à des informations supplémentaires sur les erreurs **(méthode GetLastError).** Pour plus d’informations sur la gestion des erreurs dans MAPI, voir Gestion des erreurs [dans MAPI](error-handling-in-mapi.md). 
    
- Accès aux objets implémentés par le fournisseur de services **(méthode OpenEntry).** Pour plus d’informations, voir [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).
    
- Accès à un objet d’état **(méthode OpenStatusEntry).** Pour obtenir des informations générales sur les objets d’état, voir [OBJETS D’état MAPI.](mapi-status-objects.md) Pour plus d’informations sur l’implémentation d’un objet d’état, voir [Status Object Implementation](status-object-implementation.md).
    
- Processus de ffage de logo **(méthode Logoff).** Pour plus d’informations, [voir Shutting Down a Service Provider](shutting-down-a-service-provider.md).
    
Si votre fournisseur est un fournisseur de carnet d’adresses, vous implémentez également les méthodes suivantes et les fonctionnalités associées :
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) pour fournir une liste des modèles que vous prendre en charge pour la création de destinataires. Pour plus d’informations, [voir Tableaux one-off](one-off-tables.md) ou [Implementing a Provider One-Off Table](implementing-a-provider-one-off-table.md).
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) pour fournir l’accès à l’implémentation d’un destinataire dont les données résident dans un fournisseur de carnet d’adresses hôte. Pour plus d’informations, [voir Agir en tant que fournisseur de carnet d’adresses étranger.](acting-as-a-foreign-address-book-provider.md) 
    
- [IABLogon::P repareRecips](iablogon-preparerecips.md) pour vous assurer que les propriétés appropriées sont disponibles pour tous les destinataires d’une liste de destinataires. Pour plus d’informations, [voir IABLogon::P repareRecips](iablogon-preparerecips.md). 
    
L’objet d’logon d’un fournisseur de transport, qui implémente [IXPLogon : IUnknown](ixplogoniunknown.md), est assez différent des objets d’accès implémentés par les autres types de fournisseurs de services. Il n’a que deux fonctionnalités en commun avec les autres objets d’ouverture de connecté : l’accès à un objet d’état via la méthode [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) et une opération de ffage de logo via la méthode [IXPLogon::TransportLogoff.](ixplogon-transportlogoff.md) Les fournisseurs de transport implémentent les fonctionnalités uniques suivantes dans leurs objets d’accès : 
  
- Inscription pour les types d’adresses ([méthode IXPLogon::AddressTypes).](ixplogon-addresstypes.md) Pour plus d’informations sur l’inscription d’un type d’adresse, voir Fournisseur de transport et modèle opérationnel [dupooler MAPI.](transport-provider-and-mapi-spooler-operational-model.md)
    
- Contrôle de la transmission des messages ([méthodes IXPLogon::StartMessage,](ixplogon-startmessage.md) [IXPLogon::EndMessage](ixplogon-endmessage.md)et [IXPLogon::SubmitMessage).](ixplogon-submitmessage.md) Pour plus d’informations, [voir modèle de réception de message](message-reception-model.md), Interaction avec lepooler [MAPI](interacting-with-the-mapi-spooler.md)et modèle [de soumission de messages](message-submission-model.md).
    
- Validation d’état interne ([méthode IXPLogon::ValidateState).](ixplogon-validatestate.md) 
    
- Possibilité de télécharger ou de télécharger des messages à la demande ([méthode IXPLogon::FlushQueues).](ixplogon-flushqueues.md) Pour plus d’informations, [voir Implementing the FlushQueues Method](implementing-the-flushqueues-method.md).
    
- Possibilité d’interroger les messages en attente (méthode[IXPLogon::P).](ixplogon-poll.md) Pour plus d’informations, [consultez le modèle de réception des messages.](message-reception-model.md)
    
- Détection d’état[d’inactivité ( méthode IXPLogon::Idle).](ixplogon-idle.md) 
    
- Interaction avec lepooler MAPI ([méthode IXPLogon::TransportNotify).](ixplogon-transportnotify.md) 
    
## <a name="see-also"></a>Voir aussi



[Mise en œuvre de l’logo du fournisseur de services](implementing-service-provider-logon.md)

